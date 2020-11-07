---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: B7FED447-C398-47D7-AF1B-A3E4FDAD0B41
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicappupgradeddefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppUpgradedDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppUpgradedDefinition.md
ms.openlocfilehash: 80e322fe589fbfe8d13ab9a754c98bec2fff741f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93899930"
---
# <span data-ttu-id="37a55-101">Get-AzLogicAppUpgradedDefinition</span><span class="sxs-lookup"><span data-stu-id="37a55-101">Get-AzLogicAppUpgradedDefinition</span></span>

## <span data-ttu-id="37a55-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="37a55-102">SYNOPSIS</span></span>
<span data-ttu-id="37a55-103">Получает обновленное определение для приложения логики.</span><span class="sxs-lookup"><span data-stu-id="37a55-103">Gets the upgraded definition for a logic app.</span></span>

## <span data-ttu-id="37a55-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="37a55-104">SYNTAX</span></span>

```
Get-AzLogicAppUpgradedDefinition -ResourceGroupName <String> -Name <String> -TargetSchemaVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="37a55-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="37a55-105">DESCRIPTION</span></span>
<span data-ttu-id="37a55-106">Командлет **Get-AzLogicAppUpgradedDefinition** получает обновленное определение для версии схемы и приложения логики из группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="37a55-106">The **Get-AzLogicAppUpgradedDefinition** cmdlet gets the upgraded definition for the schema version and logic app from a resource group.</span></span>
<span data-ttu-id="37a55-107">Этот командлет возвращает объект, который представляет определение обновленного логики приложения.</span><span class="sxs-lookup"><span data-stu-id="37a55-107">This cmdlet returns an object that represents the definition of the upgraded logic app.</span></span>
<span data-ttu-id="37a55-108">Укажите имя группы ресурсов, логическое имя приложения и целевую версию схемы.</span><span class="sxs-lookup"><span data-stu-id="37a55-108">Specify the resource group name, logic app name, and target schema version.</span></span>
<span data-ttu-id="37a55-109">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="37a55-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="37a55-110">Чтобы использовать динамический параметр, введите его в командную команду.</span><span class="sxs-lookup"><span data-stu-id="37a55-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="37a55-111">Чтобы найти имена динамических параметров, введите дефис (-) после имени командлета, а затем несколько раз нажмите клавишу TAB, чтобы просмотреть все доступные параметры.</span><span class="sxs-lookup"><span data-stu-id="37a55-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="37a55-112">Если вы не пропустите требуемый параметр шаблона, командлет предложит вам указать значение.</span><span class="sxs-lookup"><span data-stu-id="37a55-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="37a55-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="37a55-113">EXAMPLES</span></span>

### <span data-ttu-id="37a55-114">Пример 1: получение правила, обновленного определением приложения</span><span class="sxs-lookup"><span data-stu-id="37a55-114">Example 1: Get a logic app upgraded definition</span></span>
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

<span data-ttu-id="37a55-115">Первая команда получает определение приложения логики, которое было обновлено до указанной целевой версии схемы.</span><span class="sxs-lookup"><span data-stu-id="37a55-115">The first command gets the definition for the logic app upgraded to the specified target schema version.</span></span>
<span data-ttu-id="37a55-116">Команда хранит определение в переменной $UpgradedDefinition.</span><span class="sxs-lookup"><span data-stu-id="37a55-116">The command stores the definition in the $UpgradedDefinition variable.</span></span>
<span data-ttu-id="37a55-117">Вторая команда отображает содержимое $UpgradedDefinition в виде строки.</span><span class="sxs-lookup"><span data-stu-id="37a55-117">The second command displays the contents of $UpgradedDefinition as a string.</span></span>

## <span data-ttu-id="37a55-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="37a55-118">PARAMETERS</span></span>

### <span data-ttu-id="37a55-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37a55-119">-DefaultProfile</span></span>
<span data-ttu-id="37a55-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="37a55-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="37a55-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="37a55-121">-Name</span></span>
<span data-ttu-id="37a55-122">Указывает имя приложения логики.</span><span class="sxs-lookup"><span data-stu-id="37a55-122">Specifies the name of a logic app.</span></span>

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

### <span data-ttu-id="37a55-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37a55-123">-ResourceGroupName</span></span>
<span data-ttu-id="37a55-124">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="37a55-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="37a55-125">-TargetSchemaVersion</span><span class="sxs-lookup"><span data-stu-id="37a55-125">-TargetSchemaVersion</span></span>
<span data-ttu-id="37a55-126">Указывает целевую версию схемы для определения.</span><span class="sxs-lookup"><span data-stu-id="37a55-126">Specifies the target schema version of the definition.</span></span>

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

### <span data-ttu-id="37a55-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37a55-127">CommonParameters</span></span>
<span data-ttu-id="37a55-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="37a55-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37a55-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37a55-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37a55-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="37a55-130">INPUTS</span></span>

### <span data-ttu-id="37a55-131">System. String</span><span class="sxs-lookup"><span data-stu-id="37a55-131">System.String</span></span>

## <span data-ttu-id="37a55-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="37a55-132">OUTPUTS</span></span>

### <span data-ttu-id="37a55-133">System. Object</span><span class="sxs-lookup"><span data-stu-id="37a55-133">System.Object</span></span>

## <span data-ttu-id="37a55-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="37a55-134">NOTES</span></span>

## <span data-ttu-id="37a55-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="37a55-135">RELATED LINKS</span></span>

[<span data-ttu-id="37a55-136">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="37a55-136">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)


