<template>
    <div>
        <!-- <div> -->
            <select v-model="sellang">
                <option value="ABCabc">ABCabc</option>
                <option value="zabc">zabc</option>
                <option value="hinDi" selected>hinDi</option>
                <option value="knrra">knrra</option>
                <option value="mlyalm">mlyalm</option>
                <option value="guzraTi">guzraTi</option>
                <option value="bNgali">bNgali</option>
                <option value="Telugu">Telugu</option>
                <option value="Tmil">Tmil</option>
            		<option value="urriya">urriya</option>
                <option value="pnzabi">pnzabi</option>
                <option value="guzraTi">guzraTi</option>
                <option value="rsiAn">rsiAn</option>
            </select>
            <select v-model="selobztype">
                <option value="naun" selected>naun</option>
                <option value="pronaun">pronaun</option>
                <option value="AdzAktiv">AdzAktiv</option>
                <option value="vrb">vrb</option>
                <option value="Advrb">Advrb</option>
                <option value="prepozisn">prepozisn</option>
                <option value="knzAksn">knzAksn</option>
                <option value="kuestion">kuestion</option>
                <option value="123456789LJQWXF">123456789LJQWXF</option>
                <option value="months">months</option>
                <option value="kolors">kolors</option>
                <option value="kemikls">kemikls</option>
            </select>
            <br/>
        <div class="radio-toolbar">
          <b-modal class="u5cdot" id="modal-1" :title="sellang + ' : ' + sel_char">
            <li v-for="(imez, index) in zvrds[sellang][sel_char]" :key="index">
                <img :src="require('../assets/pikcrs/' + zimezs[imez][0] )"/>
                <p class="u5cdot">{{ zimezs[imez][1] }}</p>
            </li>
          </b-modal>
          <input type="radio" v-b-modal.modal-1  v-model="sel_char"  id="A_redio" name="redio_zabc" value="A" >
          <label for="A_redio"><div class='div_zkv'>
            <span class="indikl">&#x985;&#xA05;&#xA85;&#xB05;</span>
            <br/><span class="ssu5p">A</span> <span class="indikl">&#xD05;</span> <span class="u5cdot">A</span>
            <br/> <span class="indikl">&#x905;&#xB85;&#xC05;&#xC85;</span>
          </div></label>
          <input type="radio" v-b-modal.modal-1 v-model="sel_char" id="a_redio" name="redio_zabc" value="a">
          <label for="a_redio"><div class='div_zkv'>
            <span class="indikl">&#x986;&#xA86;&#xB06;</span>
            <br/><span class="ssu5p">a</span><span class="indikl">&#x906;&#xD06;</span><span class="u5cdot">a</span>
            <br/><span class="indikl">&#xA06;&#xB86;&#xC06;&#xC86;</span>
          </div></label>
          <input type="radio" v-b-modal.modal-1 v-model="sel_char" id="i_redio" name="redio_zabc" value="i" >
          <label for="i_redio"><div class='div_zkv'>
            <span class="indikl">&#x987;&#xA07;&#xA87;&#xB07;</span>
            <br/><span class="ssu5p">i</span> <span class="indikl">&#x907;&#xD07;</span> <span class="u5cdot">i</span>
            <br/> <span class="indikl">&#xB87;&#xC07;&#xC87;</span>
          </div></label>
          <input type="radio" v-b-modal.modal-1 v-model="sel_char" id="u_redio" name="redio_zabc" value="u">
          <label for="u_redio"><div class='div_zkv'>
            <span class="indikl">&#x989;&#xA09;&#xA89;&#xB09;&#xD09;</span>
            <br/><span class="ssu5p">u</span><span class="indikl">&#x909;&#xD09;</span><span class="u5cdot">u</span>
            <br/><span class="indikl">&#xB89;&#xC09;&#xC89;</span>
          </div></label>
          <input type="radio" v-b-modal.modal-1 v-model="sel_char" id="e_redio" name="redio_zabc" value="e" >
          <label for="e_redio"><div class='div_zkv'>
            <span class="indikl">&#x990;&#xA10;&#xA90;&#xB10;</span>
            <br/><span class="ssu5p">e</span> <span class="indikl">&#xD10;</span> <span class="u5cdot">e</span>
            <br/> <span class="indikl">&#x910;&#xB90;&#xC10;&#xC90;</span>
          </div></label>
          <input type="radio" v-b-modal.modal-1 v-model="sel_char" id="o_redio" name="redio_zabc" value="o">
          <label for="o_redio"><div class='div_zkv'>
            <span class="indikl">&#xA13;&#xA93;&#xB13;&#xD13;</span>
            <br/><span class="ssu5p">o</span><span class="indikl">&#x913;&#xD13;</span><span class="u5cdot">o</span>
            <br/><span class="indikl">&#x993;&#xB93;&#xC13;&#xC93;</span>
          </div></label>
          <!-- <br/> -->
          <input type="radio" v-b-modal.modal-1 v-model="sel_char" id="k_redio" name="redio_zabc" value="k" >
          <label for="k_redio"><div class='div_zkv'>
            <span class="indikl">&#x995;&#xA15;&#xA95;&#xB15;</span>
            <br/><span class="ssu5p">k</span> <span class="indikl">&#xD15;</span> <span class="u5cdot">k</span>
            <br/> <span class="indikl">&#x915;&#xB95;&#xC15;&#xC95;</span>
          </div></label>
          <input type="radio" v-b-modal.modal-1 v-model="sel_char" id="kh_redio" name="redio_zabc" value="kh">
          <label for="kh_redio"><div class='div_zkv'>
            <span class="indikl">&#x996;&#xA16;&#xA96;&#xB16;</span>
            <br/><span class="ssu5p">kh</span> <span class="indikl"></span> <span class="u5cdot">kh</span>
            <br/> <span class="indikl">&#x916;&#xC16;&#xC96;&#xD16;</span>
          </div></label>
          <input type="radio" v-b-modal.modal-1 v-model="sel_char" id="g_redio" name="redio_zabc" value="g" >
          <label for="g_redio"><div class='div_zkv'>
            <span class="indikl">&#x997;&#xA17;&#xA97;&#xB17;</span>
            <br/><span class="ssu5p">g</span> <span class="indikl">&#x917;</span> <span class="u5cdot">g</span>
            <br/> <span class="indikl">&#xC17;&#xC97;&#xD17;</span>
          </div></label>
          <input type="radio" v-b-modal.modal-1 v-model="sel_char" id="gh_redio" name="redio_zabc" value="gh">
          <label for="gh_redio"><div class='div_zkv'>
            <span class="indikl">&#x998;&#xA18;&#xA98;&#xB18;</span>
            <br/><span class="ssu5p">gh</span> <span class="indikl"></span> <span class="u5cdot">gh</span>
            <br/> <span class="indikl">&#x918;&#xC18;&#xC98;&#xD18;</span>
          </div></label>
          <input type="radio" v-b-modal.modal-1 v-model="sel_char" id="c_redio" name="redio_zabc" value="c" >
          <label for="c_redio"><div class='div_zkv'>
            <span class="indikl">&#x99A;&#xA1A;&#xA9A;&#xB1A;</span>
            <br/><span class="ssu5p">c</span> <span class="indikl">&#x91A;</span> <span class="u5cdot">c</span>
            <br/> <span class="indikl">&#xB9A;&#xC1A;&#xC9A;&#xD1A;</span>
          </div></label>
          <input type="radio" v-b-modal.modal-1 v-model="sel_char" id="ch_redio" name="redio_zabc" value="ch">
          <label for="ch_redio"><div class='div_zkv'>
            <span class="indikl">&#x99B;&#xA1B;&#xA9B;&#xB1B;</span>
            <br/><span class="ssu5p">ch</span> <span class="indikl"></span> <span class="u5cdot">ch</span>
            <br/> <span class="indikl">&#x91B;&#xC1B;&#xC9B;&#xD1B;</span>
          </div></label>
          <!-- <br/> -->
          <input type="radio" v-b-modal.modal-1 v-model="sel_char" id="z_redio" name="redio_zabc" value="z" >
          <label for="z_redio"><div class='div_zkv'>
            <span class="indikl">&#x99C;&#xA1C;&#xA9C;&#xB1C;</span>
            <br/><span class="ssu5p">z</span> <span class="indikl">&#xD1C;</span> <span class="u5cdot">z</span>
            <br/> <span class="indikl">&#x91C;&#xB9C;&#xC1C;&#xC9C;</span>
          </div></label>
          <input type="radio" v-b-modal.modal-1 v-model="sel_char" id="zh_redio" name="redio_zabc" value="zh" >
          <label for="zh_redio"><div class='div_zkv'>
            <span class="indikl">&#x91D;&#x99D;&#xA1D;&#xA9D;&#xB1D;</span>
            <br/><span class="ssu5p">zh</span> <span class="indikl"></span> <span class="u5cdot">zh</span>
            <br/> <span class="indikl">&#xC1D;&#xC9D;&#xD1D;</span>
          </div></label>
          <input type="radio" v-b-modal.modal-1 v-model="sel_char" id="t_redio" name="redio_zabc" value="t" >
          <label for="t_redio"><div class='div_zkv'>
            <span class="indikl">&#x99F;&#xA1F;&#xA9F;&#xB1F;</span>
            <br/><span class="ssu5p">t</span> <span class="indikl">&#x91F;</span> <span class="u5cdot">t</span>
            <br/> <span class="indikl">&#xB9F;&#xC1F;&#xC9F;&#xD1F;</span>
          </div></label>
          <input type="radio" v-b-modal.modal-1 v-model="sel_char" id="th_redio" name="redio_zabc" value="th" >
          <label for="th_redio"><div class='div_zkv'>
            <span class="indikl">&#x9A0;&#xA20;&#xAA0;&#xB20;</span>
            <br/><span class="ssu5p">th</span><span class="indikl"></span><span class="u5cdot">th</span>
            <br/> <span class="indikl">&#x920;&#xC20;&#xCA0;&#xD20;</span>
          </div></label>
          <input type="radio" v-b-modal.modal-1 v-model="sel_char" id="d_redio" name="redio_zabc" value="d" >
          <label for="d_redio"><div class='div_zkv'>
            <span class="indikl">&#x9A1;&#xA21;&#xAA1;&#xB21;</span>
            <br/><span class="ssu5p">d</span><span class="indikl">&#x921;</span><span class="u5cdot">d</span>
            <br/> <span class="indikl">&#xC21;&#xCA1;&#xD21;</span>
          </div></label>
          <input type="radio" v-b-modal.modal-1 v-model="sel_char" id="dh_redio" name="redio_zabc" value="dh" >
          <label for="dh_redio"><div class='div_zkv'>
            <span class="indikl">&#x9A2;&#xA22;&#xAA2;&#xB22;</span>
            <br/><span class="ssu5p">dh</span><span class="indikl"></span><span class="u5cdot">dh</span>
            <br/> <span class="indikl">&#x922;&#xC22;&#xCA2;&#xD22;</span>
          </div></label>
          <input type="radio" v-b-modal.modal-1 v-model="sel_char" id="T_redio" name="redio_zabc" value="T" >
          <label for="T_redio"><div class='div_zkv'>
            <span class="indikl">&#x9AA;&#xA2A;&#xAAA;&#xB2A;</span>
            <br/><span class="ssu5p">T</span><span class="indikl">&#x924;&#xD2A;</span><span class="u5cdot">T</span>
            <br/> <span class="indikl">&#xBAA;&#xC2A;&#xCAA;</span>
          </div></label>
          <input type="radio" v-b-modal.modal-1 v-model="sel_char" id="Th_redio" name="redio_zabc" value="Th" >
          <label for="Th_redio"><div class='div_zkv'>
            <span class="indikl">&#x9A5;&#xA25;&#xAA5;&#xB25;</span>
            <br/><span class="ssu5p">Th</span><span class="indikl"></span><span class="u5cdot">Th</span>
            <br/> <span class="indikl">&#x925;&#xC25;&#xCA5;&#xD25;</span>
          </div></label>
          <input type="radio" v-b-modal.modal-1 v-model="sel_char" id="D_redio" name="redio_zabc" value="D" >
          <label for="D_redio"><div class='div_zkv'>
            <span class="indikl">&#x9A6;&#xA26;&#xAA6;&#xB26;</span>
            <br/><span class="ssu5p">D</span><span class="indikl">&#x926;</span><span class="u5cdot">D</span>
            <br/> <span class="indikl">&#xC26;&#xCA6;&#xD26;</span>
          </div></label>
          <input type="radio" v-b-modal.modal-1 v-model="sel_char" id="Dh_redio" name="redio_zabc" value="Dh" >
          <label for="Dh_redio"><div class='div_zkv'>
            <span class="indikl">&#x9A7;&#xA27;&#xAA7;&#xB27;</span>
            <br/><span class="ssu5p">Dh</span><span class="u5cdot">Dh</span>
            <br/> <span class="indikl">&#x927;&#xC27;&#xCA7;&#xD27;</span>
          </div></label>
          <input type="radio" v-b-modal.modal-1 v-model="sel_char" id="n_redio" name="redio_zabc" value="n" >
          <label for="n_redio"><div class='div_zkv'>
            <span class="indikl">&#x9A8;&#xA28;&#xAA8;&#xB28;</span>
            <br/><span class="ssu5p">n</span><span class="indikl">&#x928;</span><span class="u5cdot">n</span>
            <br/> <span class="indikl">&#xC28;&#xCA8;&#xD28;</span>
          </div></label>
          <input type="radio" v-b-modal.modal-1 v-model="sel_char" id="N_redio" name="redio_zabc" value="N">
          <label for="N_redio"><div class='div_zkv'>
            <span class="indikl">&#xB02;</span>
            <br/><span class="ssu5p">N</span><span class="indikl">&#x902;</span><span class="u5cdot">N</span>
            <br/><span class="indikl">&#xB82;</span>
          </div></label>
          <input type="radio" v-b-modal.modal-1 v-model="sel_char" id="H_redio" name="redio_zabc" value="H">
          <label for="H_redio"><div class='div_zkv'>
            <span class="indikl">&#x9B9;&#xA39;&#xAB9;&#xB39;</span>
            <br/><span class="ssu5p">H</span><span class="indikl">&#x939;</span><span class="u5cdot">H</span>
            <br/> <span class="indikl">&#xC39;&#xCB9;&#xD39;</span>
          </div></label>
          <input type="radio" v-b-modal.modal-1 v-model="sel_char" id="p_redio" name="redio_zabc" value="p" >
          <label for="p_redio"><div class='div_zkv'>
            <span class="indikl">&#x9AA;&#xA2A;&#xAAA;&#xB2A;</span>
            <br/><span class="ssu5p">p</span><span class="indikl">&#x92A;&#xD2A;</span><span class="u5cdot">p</span>
            <br/> <span class="indikl">&#xBAA;&#xC2A;&#xCAA;</span>
          </div></label>
          <input type="radio" v-b-modal.modal-1 v-model="sel_char" id="ph_redio" name="redio_zabc" value="ph" >
          <label for="ph_redio"><div class='div_zkv'>
            <span class="indikl">&#x9AB;&#xA2B;&#xAAB;&#xB2B;</span>
            <br/><span class="ssu5p">ph</span><span class="u5cdot">ph</span>
            <br/> <span class="indikl">&#x92B;&#xC2B;&#xCAB;&#xD2B;</span>
          </div></label>
          <input type="radio" v-b-modal.modal-1 v-model="sel_char" id="b_redio" name="redio_zabc" value="b" >
          <label for="b_redio"><div class='div_zkv'>
            <span class="indikl">&#x9AC;&#xA2C;&#xAAC;&#xB2C;</span>
            <br/><span class="ssu5p">b</span><span class="indikl">&#x92C;</span><span class="u5cdot">b</span>
            <br/> <span class="indikl">&#xC2C;&#xCAC;&#xD2C;</span>
          </div></label>
          <input type="radio" v-b-modal.modal-1 v-model="sel_char" id="bh_redio" name="redio_zabc" value="bh" >
          <label for="bh_redio"><div class='div_zkv'>
            <span class="indikl">&#x9AD;&#xA2D;&#xAAD;&#xB2D;</span>
            <br/><span class="ssu5p">bh</span><span class="u5cdot">bh</span>
            <br/> <span class="indikl">&#x92D;&#xC2D;&#xCAD;&#xD2D;</span>
          </div></label>
          <input type="radio" v-b-modal.modal-1 v-model="sel_char" id="m_redio" name="redio_zabc" value="m" >
          <label for="m_redio"><div class='div_zkv'>
            <span class="indikl">&#x9AE;&#xA2E;&#xAAE;&#xB2E;</span>
            <br/><span class="ssu5p">m</span><span class="indikl">&#x92E;</span><span class="u5cdot">m</span>
            <br/> <span class="indikl">&#xC2E;&#xCAE;&#xD2E;</span>
          </div></label>
          <input type="radio" v-b-modal.modal-1 v-model="sel_char" id="y_redio" name="redio_zabc" value="y">
          <label for="y_redio"><div class='div_zkv'>
            <span class="indikl">&#x92F;&#x9AF;&#xA2F;&#xAAF;&#xB2F;</span>
            <br/><span class="ssu5p">y</span><span class="indikl"></span><span class="u5cdot">y</span>
            <br/> <span class="indikl">&#xC2F;&#xCAF;&#xD2F;</span>
          </div></label>
          <input type="radio" v-b-modal.modal-1 v-model="sel_char" id="h_redio" name="redio_zabc" value="h">
          <label for="h_redio"><div class='div_zkv'>
            <span class="indikl">&#x9B9;&#xA39;&#xAB9;&#xB39;</span>
            <br/><span class="ssu5p">h</span><span class="indikl">&#x939;</span><span class="u5cdot">h</span>
            <br/> <span class="indikl">&#xC39;&#xCB9;&#xD39;</span>
          </div></label>
          <!-- <br/> -->
          <input type="radio" v-b-modal.modal-1 v-model="sel_char" id="r_redio" name="redio_zabc" value="r">
          <label for="r_redio"><div class='div_zkv'>
            <span class="indikl">&#x9B0;&#xA30;&#xAB0;&#xB30;</span>
            <br/><span class="ssu5p">r</span><span class="indikl">&#x930;</span><span class="u5cdot">r</span>
            <br/> <span class="indikl">&#xC30;&#xCB0;&#xD30;</span>
          </div></label>
          <input type="radio" v-b-modal.modal-1 v-model="sel_char" id="rr_redio" name="redio_zabc" value="rr">
          <label for="rr_redio"><div class='div_zkv'>
            <span class="indikl">&#x9B0;&#xA5C;&#xAB0;&#xB5C;</span>
            <br/><span class="ssu5p">rr</span><span class="u5cdot">rr</span>
            <br/> <span class="indikl">&#x95C;&#xCB0;&#xD5C;</span>
          </div></label>
          <input type="radio" v-b-modal.modal-1 v-model="sel_char" id="l_redio" name="redio_zabc" value="l">
          <label for="l_redio"><div class='div_zkv'>
            <span class="indikl">&#x9B2;&#xA32;&#xAB2;&#xB32;</span>
            <br/><span class="ssu5p">l</span><span class="indikl">&#x932;</span><span class="u5cdot">l</span>
            <br/> <span class="indikl">&#xC32;&#xCB2;&#xD32;</span>
          </div></label>
          <input type="radio" v-b-modal.modal-1 v-model="sel_char" id="ll_redio" name="redio_zabc" value="ll">
          <label for="ll_redio"><div class='div_zkv'>
            <span class="indikl">&#xA33;&#xAB3;&#xB33;</span>
            <br/><span class="ssu5p">ll</span><span class="indikl">&#x933;</span><span class="u5cdot">ll</span>
            <br/> <span class="indikl">&#xC33;&#xCB3;&#xD33;</span>
          </div></label>
          <input type="radio" v-b-modal.modal-1 v-model="sel_char" id="v_redio" name="redio_zabc" value="v">
          <label for="v_redio"><div class='div_zkv'>
            <span class="indikl">&#xA35;&#xAB5;&#xB35;</span>
            <br/><span class="ssu5p">v</span><span class="indikl">&#x935;</span><span class="u5cdot">v</span>
            <br/> <span class="indikl">&#xC35;&#xCB5;&#xD35;</span>
          </div></label>
          <input type="radio" v-b-modal.modal-1 v-model="sel_char" id="s_redio" name="redio_zabc" value="s">
          <label for="s_redio"><div class='div_zkv'>
            <span class="indikl">&#x9B8;&#xA38;&#xAB8;&#xB38;</span>
            <br/><span class="ssu5p">s</span><span class="indikl">&#x938;</span><span class="u5cdot">s</span>
            <br/> <span class="indikl">&#xC38;&#xCB8;&#xD38;</span>
          </div></label>
          <input type="radio" v-b-modal.modal-1 v-model="sel_char" id="sh_redio" name="redio_zabc" value="sh">
          <label for="sh_redio"><div class='div_zkv'>
            <span class="indikl">&#x9B6;&#xA36;&#xAB6;&#xB36;</span>
            <br/><span class="ssu5p">sh</span><span class="indikl"></span><span class="u5cdot">sh</span>
            <br/> <span class="indikl">&#x936;&#xC36;&#xCB6;&#xD36;</span>
          </div></label>
        </div>
    </div>
</template>
<script>
// import { Meteor } from 'meteor/meteor';
  import conf from '../conf';
export default {
    name: "zkv",
    data() { return { 
      "sellang" : "hinDi", 
      "selobztype" : "0", 
      "sel_char" : "s",
      zimezs: null,
      zvrds: null
       }
    },
  async fetch() {
    this.zimezs = await this.$content(conf.zimezs).fetch();
    this.zvrds = await this.$content(conf.zvrds).fetch();
  },    
    methods: {},
    computed: {
      imezlist : function () {
        return this.zimezs[sellang][sel_char]; // not  vorking
      }
    }
}
</script>
<style>
.div_zkv { line-height: 18px; }
.ssu5p { font-family: ssu5p; font-size: 32px; font-weight:bold; color: green;}
.u5cdot { font-family: u5cdot; font-size: 24px; font-weight:bold; color: red;}
.indikl { font-size: 20px; color: #a1a; }
.radio-toolbar { margin: 1px; }
.radio-toolbar input[type="radio"] { opacity: 0; position: fixed; width: 0; }
/* .radio-toolbar input[type="radio"]:checked { opacity: 100; position: fixed; width: 0; } */
.radio-toolbar label {
  display: inline-block; background-color: #fff; padding: 2px 2px;
  border: 2px solid #44A; border-radius: 4px;
}
.radio-toolbar label:hover { background-color: cyan; }
.radio-toolbar input[type="radio"] + label { background-color: #ff0; border-color: #4cA; }
.radio-toolbar input[type="radio"]:focus + label { background-color: #fff; border: 2px dashed #000; }
</style>
