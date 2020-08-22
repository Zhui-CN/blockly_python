<template>
  <div class="hello">
    <h1>run python code in browser</h1>
    <hr/>
    <p>在浏览器中运行python代码</p>
    <div id="blocklyDiv" style="height: 600px; width: 900px;float: left;"></div>
    <xml id="toolbox" style="display: none">
      <category name="item" colour="160">
        <block type="class_block">
          <mutation>
            <arg name="scrapy.item"></arg>
          </mutation>
          <field name="NAME" value="TRUE">请输入pipelineItem名称</field>
          <comment pinned="false" h="80" w="160">描述该功能...</comment>
        </block>
        <block type="field_block"></block>
      </category>
      <category name="spider" colour="330">
        <block type="class_block">
          <mutation>
            <arg name="scrapy.Spider"></arg>
          </mutation>
          <field name="NAME" value="TRUE">请输入爬虫名称</field>
          <comment pinned="false" h="80" w="160">描述该功能...</comment>
        </block>
        <block type="variables_set">
          <field name="VAR">name</field>
          <value name="VALUE">
            <block type="text">
              <field name="TEXT"></field>
            </block>
          </value>
        </block>
        <block type="variables_set">
          <field name="VAR" variabletype>allowed_domains</field>
          <value name="VALUE">
            <block type="lists_split">
              <mutation mode="SPLIT"></mutation>
              <field name="MODE">SPLIT</field>
              <value name="INPUT">
                <block type="text">
                  <field name="TEXT"></field>
                </block>
              </value>
              <value name="DELIM">
                <shadow type="text">
                  <field name="TEXT">,</field>
                </shadow>
              </value>
            </block>
          </value>
        </block>
        <block type="variables_set">
          <field name="VAR" variabletype>start_urls</field>
          <value name="VALUE">
            <block type="lists_split">
              <mutation mode="SPLIT"></mutation>
              <field name="MODE">SPLIT</field>
              <value name="INPUT">
                <block type="text">
                  <field name="TEXT"></field>
                </block>
              </value>
              <value name="DELIM">
                <shadow type="text">
                  <field name="TEXT">,</field>
                </shadow>
              </value>
            </block>
          </value>
        </block>
        <block type="defreturn">
          <mutation>
            <arg name="self"></arg>
          </mutation>
          <field name="NAME" value="TRUE">解析函数名称</field>
          <comment pinned="false" h="80" w="160">描述该功能...</comment>
        </block>
      </category>
      <category name="test1" colour="400">
        <block type="dict_block">
          <mutation items="1"></mutation>
        </block>
        <block type="item_block"></block>
        <block type="text"></block>
        <block type="item_loader"></block>
        <block type="yield_item"></block>
        <block type="load_block">
          <value name="NAME">
            <block type="load_text"></block>
          </value>
        </block>

      </category>
      <category name="Logic" colour="210">
        <block type="controls_if"></block>
        <block type="logic_compare">
          <field name="OP">EQ</field>
        </block>
        <block type="logic_operation">
          <field name="OP">AND</field>
        </block>
        <block type="logic_negate"></block>
        <block type="logic_boolean">
          <field name="BOOL">TRUE</field>
        </block>
        <block type="logic_null"></block>
        <block type="logic_ternary"></block>
      </category>
      <category name="Loops" colour="120">
        <block type="controls_repeat_ext">
          <value name="TIMES">
            <shadow type="math_number">
              <field name="NUM">10</field>
            </shadow>
          </value>
        </block>
        <block type="controls_whileUntil">
          <field name="MODE">WHILE</field>
        </block>
        <variables>
          <variable id="/]sR^B8=bTnu8Gs]~Zr+">i</variable>
        </variables>
        <block type="controls_for">
          <field name="VAR">i</field>
          <value name="FROM">
            <shadow type="math_number">
              <field name="NUM">1</field>
            </shadow>
          </value>
          <value name="TO">
            <shadow type="math_number">
              <field name="NUM">10</field>
            </shadow>
          </value>
          <value name="BY">
            <shadow type="math_number">
              <field name="NUM">1</field>
            </shadow>
          </value>
        </block>
        <variables>
          <variable>j</variable>
        </variables>
        <block type="controls_forEach">
          <field name="VAR">j</field>
        </block>
        <block type="controls_flow_statements">
          <field name="FLOW">BREAK</field>
        </block>
      </category>
      <category name="Text" colour="160">
        <block type="text">
          <field name="TEXT"/>
        </block>
        <block type="text_join">
          <mutation items="2"/>
        </block>
        <variables>
          <variable>item</variable>
        </variables>
        <block type="text_append">
          <field name="VAR">item</field>
          <value name="TEXT">
            <shadow type="text">
              <field name="TEXT"/>
            </shadow>
          </value>
        </block>
        <block type="text_length">
          <value name="VALUE">
            <shadow type="text">
              <field name="TEXT">abc</field>
            </shadow>
          </value>
        </block>
        <block type="text_isEmpty">
          <value name="VALUE">
            <shadow type="text">
              <field name="TEXT"/>
            </shadow>
          </value>
        </block>
        <variables>
          <variable>text</variable>
        </variables>
        <block type="text_indexOf">
          <field name="END">FIRST</field>
          <value name="VALUE">
            <block type="variables_get">
              <field name="VAR">text</field>
            </block>
          </value>
          <value name="FIND">
            <shadow type="text">
              <field name="TEXT">abc</field>
            </shadow>
          </value>
        </block>
        <variables>
          <variable>text</variable>
        </variables>
        <block type="text_charAt">
          <mutation at="true"/>
          <field name="WHERE">FROM_START</field>
          <value name="VALUE">
            <block type="variables_get">
              <field name="VAR">text</field>
            </block>
          </value>
        </block>
        <variables>
          <variable>text</variable>
        </variables>
        <block type="text_getSubstring">
          <mutation at1="true" at2="true"/>
          <field name="WHERE1">FROM_START</field>
          <field name="WHERE2">FROM_START</field>
          <value name="STRING">
            <block type="variables_get">
              <field name="VAR">text</field>
            </block>
          </value>
        </block>
        <block type="text_changeCase">
            <field name="CASE">UPPERCASE</field>
            <value name="TEXT">
              <shadow type="text">
                <field name="TEXT">abc</field>
              </shadow>
            </value>
        </block>
        <block type="text_trim">
          <field name="MODE">BOTH</field>
          <value name="TEXT">
            <shadow type="text">
              <field name="TEXT">abc</field>
            </shadow>
          </value>
        </block>
        <block type="text_print">
          <value name="TEXT">
            <shadow type="text">
              <field name="TEXT">abc</field>
            </shadow>
          </value>
        </block>
        <block type="text_prompt_ext">
          <mutation type="TEXT"/>
          <field name="TYPE">TEXT</field>
          <value name="TEXT">
            <shadow type="text">
              <field name="TEXT">abc</field>
            </shadow>
          </value>
        </block>
      </category>
      <category name="Lists" colour="260">
        <block type="lists_create_with">
          <mutation items="0"/>
        </block>
        <block type="lists_create_with">
          <mutation items="0"/>
        </block>
        <block type="lists_repeat">
          <value name="NUM">
            <shadow type="math_number">
              <field name="NUM">5</field>
            </shadow>
          </value>
        </block>
        <block type="lists_length"/>
        <block type="lists_isEmpty"/>
        <variables>
          <variable>list</variable>
        </variables>
        <block type="lists_indexOf">
          <field name="END">FIRST</field>
          <value name="VALUE">
            <block type="variables_get">
              <field name="VAR">list</field>
            </block>
          </value>
        </block>
        <variables>
          <variable>list</variable>
        </variables>
        <block type="lists_getIndex">
          <mutation statement="false" at="true"/>
          <field name="MODE">GET</field>
          <field name="WHERE">FROM_START</field>
          <value name="VALUE">
            <block type="variables_get">
              <field name="VAR">list</field>
            </block>
          </value>
        </block>
        <variables>
          <variable>list</variable>
        </variables>
        <block type="lists_setIndex">
          <mutation at="true"/>
          <field name="MODE">SET</field>
          <field name="WHERE">FROM_START</field>
          <value name="LIST">
            <block type="variables_get">
              <field name="VAR">list</field>
            </block>
          </value>
        </block>
        <variables>
          <variable>list</variable>
        </variables>
        <block type="lists_getSublist">
          <mutation at1="true" at2="true"/>
          <field name="WHERE1">FROM_START</field>
          <field name="WHERE2">FROM_START</field>
          <value name="LIST">
            <block type="variables_get">
              <field name="VAR">list</field>
            </block>
          </value>
        </block>
        <block type="lists_split">
          <mutation mode="SPLIT"/>
          <field name="MODE">SPLIT</field>
          <value name="DELIM">
            <shadow type="text">
              <field name="TEXT">,</field>
            </shadow>
          </value>
        </block>
        <block type="lists_sort">
          <field name="TYPE">NUMERIC</field>
          <field name="DIRECTION">1</field>
        </block>
      </category>
      <category name="Colour" colour="20">
        <block type="colour_picker">
          <field name="COLOUR">#ff0000</field>
        </block>
        <block type="colour_random"/>
        <block type="colour_rgb">
          <value name="RED">
            <shadow type="math_number">
              <field name="NUM">100</field>
            </shadow>
          </value>
          <value name="GREEN">
            <shadow type="math_number">
              <field name="NUM">50</field>
            </shadow>
          </value>
          <value name="BLUE">
            <shadow type="math_number">
              <field name="NUM">0</field>
            </shadow>
          </value>
        </block>
        <block type="colour_blend">
          <value name="COLOUR1">
            <shadow type="colour_picker">
              <field name="COLOUR">#ff0000</field>
            </shadow>
          </value>
          <value name="COLOUR2">
            <shadow type="colour_picker">
              <field name="COLOUR">#3333ff</field>
            </shadow>
          </value>
          <value name="RATIO">
            <shadow type="math_number">
              <field name="NUM">0.5</field>
            </shadow>
          </value>
        </block>
      </category>
      <category name="Variables" colour="330" custom="VARIABLE"></category>
      <category name="Functions" colour="290" custom="PROCEDURE"></category>
    </xml>
    <textarea id="codeArea" cols="70" rows="40" style="float:left"></textarea>
  </div>
</template>

<script>
  import Blockly from 'node-blockly/browser'

  export default {
    name: 'HelloWorld',
    data() {
      return {}
    },
    mounted() {
      let that = this;
      Blockly.Blocks['class_block'] = {
        /**
         * Block for defining a procedure with no return value.
         * @this Blockly.Block
         */
        init: function () {
          var nameField = new Blockly.FieldTextInput('',
            Blockly.Procedures.rename);
          nameField.setSpellcheck(false);
          this.appendDummyInput()
            .appendField(Blockly.Msg['PROCEDURES_DEFNORETURN_TITLE'])
            .appendField(nameField, 'NAME')
            .appendField('', 'PARAMS');
          this.setMutator(new Blockly.Mutator(['procedures_mutatorarg']));
          if ((this.workspace.options.comments ||
            (this.workspace.options.parentWorkspace &&
              this.workspace.options.parentWorkspace.options.comments)) &&
            Blockly.Msg['PROCEDURES_DEFNORETURN_COMMENT']) {
            this.setCommentText(Blockly.Msg['PROCEDURES_DEFNORETURN_COMMENT']);
          }
          this.setStyle('procedure_blocks');
          this.setTooltip(Blockly.Msg['PROCEDURES_DEFNORETURN_TOOLTIP']);
          this.setHelpUrl(Blockly.Msg['PROCEDURES_DEFNORETURN_HELPURL']);
          this.arguments_ = [];
          this.argumentVarModels_ = [];
          this.setStatements_(true);
          this.statementConnection_ = null;
          this.setPreviousStatement(true, null);
          this.setNextStatement(true, null);
          this.jsonInit({
            colour: "#FFAB19"
          });
        },
        /**
         * Add or remove the statement block from this function definition.
         * @param {boolean} hasStatements True if a statement block is needed.
         * @this Blockly.Block
         */
        setStatements_: function (hasStatements) {
          if (this.hasStatements_ === hasStatements) {
            return;
          }
          if (hasStatements) {
            this.appendStatementInput('STACK')
              .appendField(Blockly.Msg['PROCEDURES_DEFNORETURN_DO']);
            if (this.getInput('RETURN')) {
              this.moveInputBefore('STACK', 'RETURN');
            }
          } else {
            this.removeInput('STACK', true);
          }
          this.hasStatements_ = hasStatements;
        },
        /**
         * Update the display of parameters for this procedure definition block.
         * @private
         * @this Blockly.Block
         */
        updateParams_: function () {

          // Merge the arguments into a human-readable list.
          var paramString = '';
          if (this.arguments_.length) {
            paramString = Blockly.Msg['PROCEDURES_BEFORE_PARAMS'] +
              ' ' + this.arguments_.join(', ');
          }
          // The params field is deterministic based on the mutation,
          // no need to fire a change event.
          Blockly.Events.disable();
          try {
            this.setFieldValue(paramString, 'PARAMS');
          } finally {
            Blockly.Events.enable();
          }
        },
        /**
         * Create XML to represent the argument inputs.
         * @param {boolean=} opt_paramIds If true include the IDs of the parameter
         *     quarks.  Used by Blockly.Procedures.mutateCallers for reconnection.
         * @return {!Element} XML storage element.
         * @this Blockly.Block
         */
        mutationToDom: function (opt_paramIds) {
          var container = document.createElement('mutation');
          if (opt_paramIds) {
            container.setAttribute('name', this.getFieldValue('NAME'));
          }
          for (var i = 0; i < this.argumentVarModels_.length; i++) {
            var parameter = document.createElement('arg');
            var argModel = this.argumentVarModels_[i];
            parameter.setAttribute('name', argModel.name);
            parameter.setAttribute('varid', argModel.getId());
            if (opt_paramIds && this.paramIds_) {
              parameter.setAttribute('paramId', this.paramIds_[i]);
            }
            container.appendChild(parameter);
          }

          // Save whether the statement input is visible.
          if (!this.hasStatements_) {
            container.setAttribute('statements', 'false');
          }
          return container;
        },
        /**
         * Parse XML to restore the argument inputs.
         * @param {!Element} xmlElement XML storage element.
         * @this Blockly.Block
         */
        domToMutation: function (xmlElement) {
          this.arguments_ = [];
          this.argumentVarModels_ = [];
          for (var i = 0, childNode; childNode = xmlElement.childNodes[i]; i++) {
            if (childNode.nodeName.toLowerCase() == 'arg') {
              var varName = childNode.getAttribute('name');
              var varId = childNode.getAttribute('varid') || childNode.getAttribute('varId');
              this.arguments_.push(varName);
              var variable = Blockly.Variables.getOrCreateVariablePackage(
                this.workspace, varId, varName, '');
              if (variable != null) {
                this.argumentVarModels_.push(variable);
              } else {
                console.log('Failed to create a variable with name ' + varName + ', ignoring.');
              }
            }
          }
          this.updateParams_();
          Blockly.Procedures.mutateCallers(this);

          // Show or hide the statement input.
          this.setStatements_(xmlElement.getAttribute('statements') !== 'false');
        },
        /**
         * Populate the mutator's dialog with this block's components.
         * @param {!Blockly.Workspace} workspace Mutator's workspace.
         * @return {!Blockly.Block} Root block in mutator.
         * @this Blockly.Block
         */
        decompose: function (workspace) {
          var containerBlock = workspace.newBlock('procedures_mutatorcontainer');
          containerBlock.initSvg();

          // Check/uncheck the allow statement box.
          if (this.getInput('RETURN')) {
            containerBlock.setFieldValue(
              this.hasStatements_ ? 'TRUE' : 'FALSE', 'STATEMENTS');
          } else {
            containerBlock.getInput('STATEMENT_INPUT').setVisible(false);
          }

          // Parameter list.
          var connection = containerBlock.getInput('STACK').connection;
          for (var i = 0; i < this.arguments_.length; i++) {
            var paramBlock = workspace.newBlock('procedures_mutatorarg');
            paramBlock.initSvg();
            paramBlock.setFieldValue(this.arguments_[i], 'NAME');
            // Store the old location.
            paramBlock.oldLocation = i;
            connection.connect(paramBlock.previousConnection);
            connection = paramBlock.nextConnection;
          }
          // Initialize procedure's callers with blank IDs.
          Blockly.Procedures.mutateCallers(this);
          return containerBlock;
        },
        /**
         * Reconfigure this block based on the mutator dialog's components.
         * @param {!Blockly.Block} containerBlock Root block in mutator.
         * @this Blockly.Block
         */
        compose: function (containerBlock) {
          // Parameter list.
          this.arguments_ = [];
          this.paramIds_ = [];
          this.argumentVarModels_ = [];
          var paramBlock = containerBlock.getInputTargetBlock('STACK');
          while (paramBlock) {
            var varName = paramBlock.getFieldValue('NAME');
            this.arguments_.push(varName);
            var variable = this.workspace.getVariable(varName, '');
            if (variable != null) {
              this.argumentVarModels_.push(variable);
            } else {
              console.log('Failed to get variable named ' + varName + ', ignoring.');
            }

            this.paramIds_.push(paramBlock.id);
            paramBlock = paramBlock.nextConnection &&
              paramBlock.nextConnection.targetBlock();
          }
          this.updateParams_();
          Blockly.Procedures.mutateCallers(this);

          // Show/hide the statement input.
          var hasStatements = containerBlock.getFieldValue('STATEMENTS');
          if (hasStatements !== null) {
            hasStatements = hasStatements == 'TRUE';
            if (this.hasStatements_ != hasStatements) {
              if (hasStatements) {
                this.setStatements_(true);
                // Restore the stack, if one was saved.
                Blockly.Mutator.reconnect(this.statementConnection_, this, 'STACK');
                this.statementConnection_ = null;
              } else {
                // Save the stack, then disconnect it.
                var stackConnection = this.getInput('STACK').connection;
                this.statementConnection_ = stackConnection.targetConnection;
                if (this.statementConnection_) {
                  var stackBlock = stackConnection.targetBlock();
                  stackBlock.unplug();
                  stackBlock.bumpNeighbours_();
                }
                this.setStatements_(false);
              }
            }
          }
        },
        /**
         * Return the signature of this procedure definition.
         * @return {!Array} Tuple containing three elements:
         *     - the name of the defined procedure,
         *     - a list of all its arguments,
         *     - that it DOES NOT have a return value.
         * @this Blockly.Block
         */
        getProcedureDef: function () {
          return [this.getFieldValue('NAME'), this.arguments_, false];
        },
        /**
         * Return all variables referenced by this block.
         * @return {!Array.<string>} List of variable names.
         * @this Blockly.Block
         */
        getVars: function () {
          return this.arguments_;
        },
        /**
         * Return all variables referenced by this block.
         * @return {!Array.<!Blockly.VariableModel>} List of variable models.
         * @this Blockly.Block
         */
        getVarModels: function () {
          return this.argumentVarModels_;
        },
        /**
         * Notification that a variable is renaming.
         * If the ID matches one of this block's variables, rename it.
         * @param {string} oldId ID of variable to rename.
         * @param {string} newId ID of new variable.  May be the same as oldId, but
         *     with an updated name.  Guaranteed to be the same type as the old
         *     variable.
         * @override
         * @this Blockly.Block
         */
        renameVarById: function (oldId, newId) {
          var oldVariable = this.workspace.getVariableById(oldId);
          if (oldVariable.type != '') {
            // Procedure arguments always have the empty type.
            return;
          }
          var oldName = oldVariable.name;
          var newVar = this.workspace.getVariableById(newId);

          var change = false;
          for (var i = 0; i < this.argumentVarModels_.length; i++) {
            if (this.argumentVarModels_[i].getId() == oldId) {
              this.arguments_[i] = newVar.name;
              this.argumentVarModels_[i] = newVar;
              change = true;
            }
          }
          if (change) {
            this.displayRenamedVar_(oldName, newVar.name);
            Blockly.Procedures.mutateCallers(this);
          }
        },
        /**
         * Notification that a variable is renaming but keeping the same ID.  If the
         * variable is in use on this block, rerender to show the new name.
         * @param {!Blockly.VariableModel} variable The variable being renamed.
         * @package
         * @override
         * @this Blockly.Block
         */
        updateVarName: function (variable) {
          var newName = variable.name;
          var change = false;
          for (var i = 0; i < this.argumentVarModels_.length; i++) {
            if (this.argumentVarModels_[i].getId() == variable.getId()) {
              var oldName = this.arguments_[i];
              this.arguments_[i] = newName;
              change = true;
            }
          }
          if (change) {
            this.displayRenamedVar_(oldName, newName);
            Blockly.Procedures.mutateCallers(this);
          }
        },
        /**
         * Update the display to reflect a newly renamed argument.
         * @param {string} oldName The old display name of the argument.
         * @param {string} newName The new display name of the argument.
         * @private
         */
        displayRenamedVar_: function (oldName, newName) {
          this.updateParams_();
          // Update the mutator's variables if the mutator is open.
          if (this.mutator.isVisible()) {
            var blocks = this.mutator.workspace_.getAllBlocks(false);
            for (var i = 0, block; block = blocks[i]; i++) {
              if (block.type == 'procedures_mutatorarg' &&
                Blockly.Names.equals(oldName, block.getFieldValue('NAME'))) {
                block.setFieldValue(newName, 'NAME');
              }
            }
          }
        },
        /**
         * Add custom menu options to this block's context menu.
         * @param {!Array} options List of menu options to add to.
         * @this Blockly.Block
         */
        customContextMenu: function (options) {
          if (this.isInFlyout) {
            return;
          }
          // Add option to create caller.
          var option = {enabled: true};
          var name = this.getFieldValue('NAME');
          option.text = Blockly.Msg['PROCEDURES_CREATE_DO'].replace('%1', name);
          var xmlMutation = document.createElement('mutation');
          xmlMutation.setAttribute('name', name);
          for (var i = 0; i < this.arguments_.length; i++) {
            var xmlArg = document.createElement('arg');
            xmlArg.setAttribute('name', this.arguments_[i]);
            xmlMutation.appendChild(xmlArg);
          }
          var xmlBlock = document.createElement('block');
          xmlBlock.setAttribute('type', this.callType_);
          xmlBlock.appendChild(xmlMutation);
          option.callback = Blockly.ContextMenu.callbackFactory(this, xmlBlock);
          options.push(option);

          // Add options to create getters for each parameter.
          if (!this.isCollapsed()) {
            for (var i = 0; i < this.argumentVarModels_.length; i++) {
              var option = {enabled: true};
              var argVar = this.argumentVarModels_[i];
              var name = argVar.name;
              option.text = Blockly.Msg['VARIABLES_SET_CREATE_GET'].replace('%1', name);

              var xmlField = Blockly.Variables.generateVariableFieldDom(argVar);
              var xmlBlock = document.createElement('block');
              xmlBlock.setAttribute('type', 'variables_get');
              xmlBlock.appendChild(xmlField);
              option.callback = Blockly.ContextMenu.callbackFactory(this, xmlBlock);
              options.push(option);
            }
          }
        },
        callType_: 'procedures_callnoreturn'
      };
      Blockly.Python["class_block"] = function (block) {
        // let statements_name = Blockly.Python.statementToCode(block, "do");
        let statements_name = Blockly.Python.statementToCode(block, "STACK");
        let args = block["arguments_"].toString();
        let function_name = block["inputList"][0]["fieldRow"][1]["text_"];
        return "class " + function_name + "(" + args + "):\n" + statements_name + "\n\n";
      };

      Blockly.Blocks["field_block"] = {
        init: function () {
          this.jsonInit({
            type: "field_block",
            message0: "%1",
            args0: [{
              type: "field_input",
              name: "TEXT",
              text: "请输入字段"
            }],
            previousStatement: null,
            nextStatement: null,
            colour: "#AABB11",
          });
        }
      };
      Blockly.Python['field_block'] = function (block) {
        return block.getFieldValue("TEXT") + " = scrapy.Field()\n";
      };

      Blockly.Blocks['defreturn'] = {
        /**
         * Block for defining a procedure with a return value.
         * @this Blockly.Block
         */
        init: function () {
          var nameField = new Blockly.FieldTextInput('',
            Blockly.Procedures.rename);
          nameField.setSpellcheck(false);
          this.appendDummyInput()
            .appendField(Blockly.Msg['PROCEDURES_DEFRETURN_TITLE'])
            .appendField(nameField, 'NAME')
            .appendField('', 'PARAMS');
          this.appendValueInput('RETURN')
            .setAlign(Blockly.ALIGN_RIGHT)
            .appendField(Blockly.Msg['PROCEDURES_DEFRETURN_RETURN']);
          this.setMutator(new Blockly.Mutator(['procedures_mutatorarg']));
          if ((this.workspace.options.comments ||
            (this.workspace.options.parentWorkspace &&
              this.workspace.options.parentWorkspace.options.comments)) &&
            Blockly.Msg['PROCEDURES_DEFRETURN_COMMENT']) {
            this.setCommentText(Blockly.Msg['PROCEDURES_DEFRETURN_COMMENT']);
          }
          this.setStyle('procedure_blocks');
          this.setTooltip(Blockly.Msg['PROCEDURES_DEFRETURN_TOOLTIP']);
          this.setHelpUrl(Blockly.Msg['PROCEDURES_DEFRETURN_HELPURL']);
          this.arguments_ = [];
          this.argumentVarModels_ = [];
          this.setStatements_(true);
          this.statementConnection_ = null;
          this.setPreviousStatement(true, null);
          this.setNextStatement(true, null);
        },
        setStatements_: Blockly.Blocks['procedures_defnoreturn'].setStatements_,
        updateParams_: Blockly.Blocks['procedures_defnoreturn'].updateParams_,
        mutationToDom: Blockly.Blocks['procedures_defnoreturn'].mutationToDom,
        domToMutation: Blockly.Blocks['procedures_defnoreturn'].domToMutation,
        decompose: Blockly.Blocks['procedures_defnoreturn'].decompose,
        compose: Blockly.Blocks['procedures_defnoreturn'].compose,
        /**
         * Return the signature of this procedure definition.
         * @return {!Array} Tuple containing three elements:
         *     - the name of the defined procedure,
         *     - a list of all its arguments,
         *     - that it DOES have a return value.
         * @this Blockly.Block
         */
        getProcedureDef: function () {
          return [this.getFieldValue('NAME'), this.arguments_, true];
        },
        getVars: Blockly.Blocks['procedures_defnoreturn'].getVars,
        getVarModels: Blockly.Blocks['procedures_defnoreturn'].getVarModels,
        renameVarById: Blockly.Blocks['procedures_defnoreturn'].renameVarById,
        updateVarName: Blockly.Blocks['procedures_defnoreturn'].updateVarName,
        displayRenamedVar_: Blockly.Blocks['procedures_defnoreturn'].displayRenamedVar_,
        customContextMenu: Blockly.Blocks['procedures_defnoreturn'].customContextMenu,
        callType_: 'procedures_callreturn'
      };
      Blockly.Python['defreturn'] = function (block) {
        let statements_name = Blockly.Python.statementToCode(block, "STACK");
        let args = block["arguments_"].toString();
        let function_name = block["inputList"][0]["fieldRow"][1]["text_"];
        let returnValue = Blockly.Python.valueToCode(block, 'RETURN',
          Blockly.Python.ORDER_NONE) || ''
        if (returnValue) {
          return "def " + function_name + "(" + args + "):\n" + statements_name + "  yield " + returnValue + "\n\n";
        } else {
          return "def " + function_name + "(" + args + "):\n" + statements_name + "\n\n";
        }
      };

      Blockly.Blocks['dict_block'] = {
        /**
         * Block for creating a list with any number of elements of any type.
         * @this Blockly.Block
         */
        init: function () {
          this.appendDummyInput()
            .appendField(new Blockly.FieldTextInput("嵌套的key"), "NAME");
          this.setHelpUrl(Blockly.Msg['LISTS_CREATE_WITH_HELPURL']);
          this.setStyle('list_blocks');
          this.itemCount_ = 3;
          this.updateShape_();
          this.setOutput(true, 'Array');
          this.setMutator(new Blockly.Mutator(['lists_create_with_item']));
          this.setTooltip(Blockly.Msg['LISTS_CREATE_WITH_TOOLTIP']);
        },
        /**
         * Create XML to represent list inputs.
         * @return {!Element} XML storage element.
         * @this Blockly.Block
         */
        mutationToDom: function () {
          var container = document.createElement('mutation');
          container.setAttribute('items', this.itemCount_);
          return container;
        },
        /**
         * Parse XML to restore the list inputs.
         * @param {!Element} xmlElement XML storage element.
         * @this Blockly.Block
         */
        domToMutation: function (xmlElement) {
          this.itemCount_ = parseInt(xmlElement.getAttribute('items'), 10);
          this.updateShape_();
        },
        /**
         * Populate the mutator's dialog with this block's components.
         * @param {!Blockly.Workspace} workspace Mutator's workspace.
         * @return {!Blockly.Block} Root block in mutator.
         * @this Blockly.Block
         */
        decompose: function (workspace) {
          var containerBlock = workspace.newBlock('lists_create_with_container');
          containerBlock.initSvg();
          var connection = containerBlock.getInput('STACK').connection;
          for (var i = 0; i < this.itemCount_; i++) {
            var itemBlock = workspace.newBlock('lists_create_with_item');
            itemBlock.initSvg();
            connection.connect(itemBlock.previousConnection);
            connection = itemBlock.nextConnection;
          }
          return containerBlock;
        },
        /**
         * Reconfigure this block based on the mutator dialog's components.
         * @param {!Blockly.Block} containerBlock Root block in mutator.
         * @this Blockly.Block
         */
        compose: function (containerBlock) {
          var itemBlock = containerBlock.getInputTargetBlock('STACK');
          // Count number of inputs.
          var connections = [];
          while (itemBlock) {
            connections.push(itemBlock.valueConnection_);
            itemBlock = itemBlock.nextConnection &&
              itemBlock.nextConnection.targetBlock();
          }
          // Disconnect any children that don't belong.
          for (var i = 0; i < this.itemCount_; i++) {
            var connection = this.getInput('ADD' + i).connection.targetConnection;
            if (connection && connections.indexOf(connection) == -1) {
              connection.disconnect();
            }
          }
          this.itemCount_ = connections.length;
          this.updateShape_();
          // Reconnect any child blocks.
          for (var i = 0; i < this.itemCount_; i++) {
            Blockly.Mutator.reconnect(connections[i], this, 'ADD' + i);
          }
        },
        /**
         * Store pointers to any connected child blocks.
         * @param {!Blockly.Block} containerBlock Root block in mutator.
         * @this Blockly.Block
         */
        saveConnections: function (containerBlock) {
          var itemBlock = containerBlock.getInputTargetBlock('STACK');
          var i = 0;
          while (itemBlock) {
            var input = this.getInput('ADD' + i);
            itemBlock.valueConnection_ = input && input.connection.targetConnection;
            i++;
            itemBlock = itemBlock.nextConnection &&
              itemBlock.nextConnection.targetBlock();
          }
        },
        /**
         * Modify this block to have the correct number of inputs.
         * @private
         * @this Blockly.Block
         */
        updateShape_: function () {
          if (this.itemCount_ && this.getInput('EMPTY')) {
            this.removeInput('EMPTY');
          } else if (!this.itemCount_ && !this.getInput('EMPTY')) {
            this.appendDummyInput('EMPTY')
              .appendField('空');
            // .appendField(Blockly.Msg['LISTS_CREATE_EMPTY_TITLE']);
          }
          // Add new inputs.
          for (var i = 0; i < this.itemCount_; i++) {
            if (!this.getInput('ADD' + i)) {
              var input = this.appendValueInput('ADD' + i);
              if (i == 0) {
                input.appendField('建立字典');
                // input.appendField(Blockly.Msg['LISTS_CREATE_WITH_INPUT_WITH']);
              }
            }
          }
          // Remove deleted inputs.
          while (this.getInput('ADD' + i)) {
            this.removeInput('ADD' + i);
            i++;
          }
        }
      };
      Blockly.Python['dict_block'] = function (block) {
        // let statements_name = Blockly.Python.statementToCode(block, "STACK");
        // let new_list = [];
        // let new_str = "";
        // let childBlocks = block['childBlocks_'];
        // for (var i = 0; i < childBlocks.length; i++) {
        //   new_str = "";
        //   var fieldRow = childBlocks[i]['inputList'][0]['fieldRow']
        //   for (var j = 0; j < fieldRow.length; j++) {
        //     new_str += fieldRow[j]['text_'];
        //   }
        //   new_list.push(new_str);
        // }
        // console.log(block)
        // console.log(new_list);
        // // return ["{" + new_list.toString() + "}", Blockly.Python.ORDER_ATOMIC];
        // // return "{" + new_list.toString() + "}" + statements_name;
        // return statements_name + "{" + new_list.toString() + "}";var elements = new Array(block.itemCount_);
        var elements = new Array(block.itemCount_);
        for (var i = 0; i < block.itemCount_; i++) {
          elements[i] = Blockly.Python.valueToCode(block, 'ADD' + i,
            Blockly.Python.ORDER_NONE).replace("{","").replace("}","") || '';
          console.log(elements[i])
        }
        var nesting_name = block['inputList'][0]['fieldRow'][0]['text_'];
        if (nesting_name !== "嵌套的key"){
          return [nesting_name + ': {' + elements.join(', ') + '}', Blockly.Python.ORDER_ATOMIC];
        }
        nesting_name = '';
        return [nesting_name + '{' + elements.join(', ') + '}', Blockly.Python.ORDER_ATOMIC];
      };

      Blockly.Blocks["item_block"] = {
        init: function () {
          this.jsonInit({
            message0: "%1 : %2",
            args0: [
              {
                type: "field_input",
                name: "key",
                text: "key"
                // variable: "key"
              },
              {
                type: "field_input",
                name: "value",
                text: "value"
                // variable: "value"
              }
            ],
            colour: "#AABB11",
            output: null
          });
        }
      };
      Blockly.Python["item_block"] = function (block) {
        console.log(block);
        let key = Blockly.Python.quote_(block.getFieldValue('key'))
        let value = Blockly.Python.quote_(block.getFieldValue('value'))
        return ['{' + key + ':' + value + '}', Blockly.Python.ORDER_ATOMIC];
      };

      Blockly.Blocks["load_text"] = {
        init: function () {
          this.jsonInit({
            message0: "%1  %2  %3  %4",
            args0: [
              {
                type: "field_input",
                name: "name",
                text: "请输入字段"
              },
              {
                type: "field_input",
                name: "value",
                text: "值"
              },
              {
                type: "field_input",
                name: "processor",
                text: "处理器"
              },
              {
                type: "field_input",
                name: "re",
                text: "正则表达式"
              }
            ],
            "colour": 180,
            output: null
          });
        }
      };
      Blockly.Blocks["load_block"] = {
        init: function () {
          this.jsonInit({
            "type": "load_block",
            "message0": "%1 %2",
            "args0": [
              {
                "type": "field_dropdown",
                "name": "select",
                "options": [
                  ["XPATH", "xpath"],
                  ["CSS", "css"]
                ]
              },
              {
                "type": "input_value",
                "name": "NAME"
              }
            ],
            "previousStatement": null,
            "nextStatement": null,
            "colour": 180,
          });
        }
      };
      Blockly.Python['load_block'] = function (block) {
        try{
          var fieldRows = block['childBlocks_'][0]['inputList'][0]['fieldRow'];
          for (var i = 0; i < fieldRows.length; i++) {
            if (that.in_arry(fieldRows[i]['text_'])){
              fieldRows[i]['text_'] = "";
            }
          }
        }catch (e) {
          return "";
        }
        var name = Blockly.Python.quote_(fieldRows[0]['text_']);
        var value = Blockly.Python.quote_(fieldRows[1]['text_']);
        var processor = Blockly.Python.quote_(fieldRows[2]['text_']);
        var re = "re=" + Blockly.Python.quote_(fieldRows[3]['text_']);
        var select = block.getFieldValue('select');
        return "loader.add_" + select + "(" + name +  "," + value + "," + processor + "," + re + ")\n";
      };

      Blockly.Blocks["item_loader"] = {
        init: function () {
          this.jsonInit({
            type: "item_loader",
            message0: "%1",
            args0: [{
              type: "field_input",
              name: "TEXT",
              text: "请输入item名称"
            }],
            previousStatement: null,
            nextStatement: null,
            colour: 30,
          });
        }
      };
      Blockly.Python['item_loader'] = function (block) {
        return "loader = ItemLoader(item=" + block.getFieldValue("TEXT") + "(), response=response)\n";
      };

      Blockly.Blocks["yield_item"] = {
        init: function () {
          this.jsonInit({
            message0: "交 出 item",
            colour: 0,
            output: null
          });
        }
      };
      Blockly.Python["yield_item"] = function (block) {
        // var code = Blockly.Python.quote_(block.getFieldValue('TEXT'));
        return ["loader.load_item()", Blockly.Python.ORDER_ATOMIC];
      };

      let demoWorkspace = Blockly.inject("blocklyDiv", {
        media: "../../node_modules/node-blockly/blockly/media/",
        toolbox: document.getElementById("toolbox"),
        // 缩放
        zoom: {
          controls: true,
          wheel: true,
          startScale: 1.0,
          maxScale: 3,
          minScale: 0.3,
          scaleSpeed: 1.2
        },
        // 网格
        grid: {
          spacing: 20,
          length: 3,
          colour: "#ccc",
          snap: true
        }
      });
      demoWorkspace.addChangeListener(event => {
        // 工作区转代码
        document.getElementById("codeArea").value = Blockly.Python.workspaceToCode(demoWorkspace);
      });
    },
    methods: {
      in_arry(data) {
        let testdata = ["请输入字段", "值", "处理器", "正则表达式"];
        for (var i = 0; i < testdata.length; i++){
          if (data === testdata[i]){
            return true;
          }
        }
      }
    }
  }
</script>
