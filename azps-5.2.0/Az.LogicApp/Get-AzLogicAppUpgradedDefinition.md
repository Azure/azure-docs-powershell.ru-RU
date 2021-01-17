---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: B7FED447-C398-47D7-AF1B-A3E4FDAD0B41
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicappupgradeddefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppUpgradedDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppUpgradedDefinition.md
ms.openlocfilehash: 2c0eb437aaa8a280b970e9c2a210b37b8fbce2d8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98413295"
---
# <span data-ttu-id="66bf7-101">Get-AzLogicAppUpgradedDefinition</span><span class="sxs-lookup"><span data-stu-id="66bf7-101">Get-AzLogicAppUpgradedDefinition</span></span>

## <span data-ttu-id="66bf7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66bf7-102">SYNOPSIS</span></span>
<span data-ttu-id="66bf7-103">Возвращает обновленное определение для приложения логики.</span><span class="sxs-lookup"><span data-stu-id="66bf7-103">Gets the upgraded definition for a logic app.</span></span>

## <span data-ttu-id="66bf7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="66bf7-104">SYNTAX</span></span>

```
Get-AzLogicAppUpgradedDefinition -ResourceGroupName <String> -Name <String> -TargetSchemaVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66bf7-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="66bf7-105">DESCRIPTION</span></span>
<span data-ttu-id="66bf7-106">**Cmdlet Get-AzLogicAppUpgradedDefinition** получает обновленное определение для версии схемы и приложения логики из группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="66bf7-106">The **Get-AzLogicAppUpgradedDefinition** cmdlet gets the upgraded definition for the schema version and logic app from a resource group.</span></span>
<span data-ttu-id="66bf7-107">Этот cmdlet возвращает объект, который представляет определение обновленного приложения логики.</span><span class="sxs-lookup"><span data-stu-id="66bf7-107">This cmdlet returns an object that represents the definition of the upgraded logic app.</span></span>
<span data-ttu-id="66bf7-108">Укажите имя группы ресурсов, имя приложения логики и версию целевой схемы.</span><span class="sxs-lookup"><span data-stu-id="66bf7-108">Specify the resource group name, logic app name, and target schema version.</span></span>
<span data-ttu-id="66bf7-109">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="66bf7-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="66bf7-110">Чтобы использовать динамический параметр, введите его в команду.</span><span class="sxs-lookup"><span data-stu-id="66bf7-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="66bf7-111">Чтобы найти имена динамических параметров, введите дефис (-) после имени cmdlet, а затем нажимая клавишу TAB для циклическиго перебора доступных параметров.</span><span class="sxs-lookup"><span data-stu-id="66bf7-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="66bf7-112">Если параметр обязательного шаблона не задан, будет выдан запрос на его значение.</span><span class="sxs-lookup"><span data-stu-id="66bf7-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="66bf7-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="66bf7-113">EXAMPLES</span></span>

### <span data-ttu-id="66bf7-114">Пример 1. Обновление определения приложения для логики</span><span class="sxs-lookup"><span data-stu-id="66bf7-114">Example 1: Get a logic app upgraded definition</span></span>
```
PS C:\>$UpgradedDefinition = Get-AzLogicAppUpgradedDefinition -ResourceGroupName "ResourceGroup11" -Name "LogicApp01" -TargetSchemaVersion "2016-06-01"
$UpgradedDefinition.ToString()
{

  "$schema": "http://schema.management.azure.com/providers/Microsoft.Logic/schemas/2016-06-01/workflowdefinition.json#",

  "contentVersion": "1.0.0.0",

  "parameters": {},

  "triggers": {

    "httpTrigger": {

      "recurrence": {

        "frequency": "Hour",

        "interval": 1

      },

      "type": "Http",

      "inputs": {

        "method": "GET",

        "uri": "http://www.bing.com"

      },

      "conditions": [

        {

          "expression": "@bool('true')" 

        }

      ] 

    },

    "manualTrigger": {

      "type": "Request",

      "kind": "Http"

    }

  },

  "actions": {

    "httpScope": {

      "actions": {

        "http": {

          "runAfter": {},

          "type": "Http",

          "inputs": {

            "method": "GET",

            "uri": "http://www.bing.com"

          }

        }

      },

      "runAfter": {},

      "else": {

        "actions": {}

      },

      "expression": "@bool('true')", 

      "type": "If"

    },

    "http1Scope": {

      "actions": {

        "http1": {

          "runAfter": {},

          "type": "Http",

          "inputs": {

            "method": "GET",

            "uri": "http://www.bing.com"

          }

        }

      },

      "runAfter": {},

      "else": {

        "actions": {}

      },

      "expression": "@bool('true')", 

      "type": "If"

    }

  },

  "outputs": {

    "output1": {

      "type": "String",

      "value": "true"

    }

  }

}
```

<span data-ttu-id="66bf7-115">Первая команда получает определение для приложения логики, обновленного до указанной целевой версии схемы.</span><span class="sxs-lookup"><span data-stu-id="66bf7-115">The first command gets the definition for the logic app upgraded to the specified target schema version.</span></span>
<span data-ttu-id="66bf7-116">Команда хранит определение в переменной $UpgradedDefinition.</span><span class="sxs-lookup"><span data-stu-id="66bf7-116">The command stores the definition in the $UpgradedDefinition variable.</span></span>
<span data-ttu-id="66bf7-117">Вторая команда отображает содержимое $UpgradedDefinition как строку.</span><span class="sxs-lookup"><span data-stu-id="66bf7-117">The second command displays the contents of $UpgradedDefinition as a string.</span></span>

## <span data-ttu-id="66bf7-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="66bf7-118">PARAMETERS</span></span>

### <span data-ttu-id="66bf7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66bf7-119">-DefaultProfile</span></span>
<span data-ttu-id="66bf7-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="66bf7-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66bf7-121">-Name</span><span class="sxs-lookup"><span data-stu-id="66bf7-121">-Name</span></span>
<span data-ttu-id="66bf7-122">Указывает имя приложения логики.</span><span class="sxs-lookup"><span data-stu-id="66bf7-122">Specifies the name of a logic app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66bf7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66bf7-123">-ResourceGroupName</span></span>
<span data-ttu-id="66bf7-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="66bf7-124">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66bf7-125">-TargetSchemaVersion</span><span class="sxs-lookup"><span data-stu-id="66bf7-125">-TargetSchemaVersion</span></span>
<span data-ttu-id="66bf7-126">Определяет целевую версию схемы определения.</span><span class="sxs-lookup"><span data-stu-id="66bf7-126">Specifies the target schema version of the definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66bf7-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66bf7-127">CommonParameters</span></span>
<span data-ttu-id="66bf7-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66bf7-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66bf7-129">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66bf7-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66bf7-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="66bf7-130">INPUTS</span></span>

### <span data-ttu-id="66bf7-131">System.String</span><span class="sxs-lookup"><span data-stu-id="66bf7-131">System.String</span></span>

## <span data-ttu-id="66bf7-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="66bf7-132">OUTPUTS</span></span>

### <span data-ttu-id="66bf7-133">System.Object</span><span class="sxs-lookup"><span data-stu-id="66bf7-133">System.Object</span></span>

## <span data-ttu-id="66bf7-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="66bf7-134">NOTES</span></span>

## <span data-ttu-id="66bf7-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="66bf7-135">RELATED LINKS</span></span>

[<span data-ttu-id="66bf7-136">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="66bf7-136">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)


