---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: B7FED447-C398-47D7-AF1B-A3E4FDAD0B41
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppUpgradedDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppUpgradedDefinition.md
ms.openlocfilehash: fda0c69f1df7df0939af3b788354111ddbaf8471
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734824"
---
# <span data-ttu-id="07261-101">Get-AzureRmLogicAppUpgradedDefinition</span><span class="sxs-lookup"><span data-stu-id="07261-101">Get-AzureRmLogicAppUpgradedDefinition</span></span>

## <span data-ttu-id="07261-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="07261-102">SYNOPSIS</span></span>
<span data-ttu-id="07261-103">Получает обновленное определение для приложения логики.</span><span class="sxs-lookup"><span data-stu-id="07261-103">Gets the upgraded definition for a logic app.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="07261-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="07261-104">SYNTAX</span></span>

```
Get-AzureRmLogicAppUpgradedDefinition -ResourceGroupName <String> -Name <String> -TargetSchemaVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07261-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="07261-105">DESCRIPTION</span></span>
<span data-ttu-id="07261-106">Командлет **Get-AzureRmLogicAppUpgradedDefinition** получает обновленное определение для версии схемы и приложения логики из группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="07261-106">The **Get-AzureRmLogicAppUpgradedDefinition** cmdlet gets the upgraded definition for the schema version and logic app from a resource group.</span></span>
<span data-ttu-id="07261-107">Этот командлет возвращает объект, который представляет определение обновленного логики приложения.</span><span class="sxs-lookup"><span data-stu-id="07261-107">This cmdlet returns an object that represents the definition of the upgraded logic app.</span></span>
<span data-ttu-id="07261-108">Укажите имя группы ресурсов, логическое имя приложения и целевую версию схемы.</span><span class="sxs-lookup"><span data-stu-id="07261-108">Specify the resource group name, logic app name, and target schema version.</span></span>

<span data-ttu-id="07261-109">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="07261-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="07261-110">Чтобы использовать динамический параметр, введите его в командную команду.</span><span class="sxs-lookup"><span data-stu-id="07261-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="07261-111">Чтобы найти имена динамических параметров, введите дефис (-) после имени командлета, а затем несколько раз нажмите клавишу TAB, чтобы просмотреть все доступные параметры.</span><span class="sxs-lookup"><span data-stu-id="07261-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="07261-112">Если вы не пропустите требуемый параметр шаблона, командлет предложит вам указать значение.</span><span class="sxs-lookup"><span data-stu-id="07261-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="07261-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="07261-113">EXAMPLES</span></span>

### <span data-ttu-id="07261-114">Пример 1: получение правила, обновленного определением приложения</span><span class="sxs-lookup"><span data-stu-id="07261-114">Example 1: Get a logic app upgraded definition</span></span>
```
PS C:\>$UpgradedDefinition = Get-AzureRmLogicAppUpgradedDefinition -ResourceGroupName "ResourceGroup11" -Name "LogicApp01" -TargetSchemaVersion "2016-06-01"
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

<span data-ttu-id="07261-115">Первая команда получает определение приложения логики, которое было обновлено до указанной целевой версии схемы.</span><span class="sxs-lookup"><span data-stu-id="07261-115">The first command gets the definition for the logic app upgraded to the specified target schema version.</span></span>
<span data-ttu-id="07261-116">Команда хранит определение в переменной $UpgradedDefinition.</span><span class="sxs-lookup"><span data-stu-id="07261-116">The command stores the definition in the $UpgradedDefinition variable.</span></span>

<span data-ttu-id="07261-117">Вторая команда отображает содержимое $UpgradedDefinition в виде строки.</span><span class="sxs-lookup"><span data-stu-id="07261-117">The second command displays the contents of $UpgradedDefinition as a string.</span></span>

## <span data-ttu-id="07261-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="07261-118">PARAMETERS</span></span>

### <span data-ttu-id="07261-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="07261-119">-Name</span></span>
<span data-ttu-id="07261-120">Указывает имя приложения логики.</span><span class="sxs-lookup"><span data-stu-id="07261-120">Specifies the name of a logic app.</span></span>

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

### <span data-ttu-id="07261-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07261-121">-ResourceGroupName</span></span>
<span data-ttu-id="07261-122">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="07261-122">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="07261-123">-TargetSchemaVersion</span><span class="sxs-lookup"><span data-stu-id="07261-123">-TargetSchemaVersion</span></span>
<span data-ttu-id="07261-124">Указывает целевую версию схемы для определения.</span><span class="sxs-lookup"><span data-stu-id="07261-124">Specifies the target schema version of the definition.</span></span>

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

### <span data-ttu-id="07261-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07261-125">-DefaultProfile</span></span>
<span data-ttu-id="07261-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="07261-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07261-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07261-127">CommonParameters</span></span>
<span data-ttu-id="07261-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="07261-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07261-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07261-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07261-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="07261-130">INPUTS</span></span>

## <span data-ttu-id="07261-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="07261-131">OUTPUTS</span></span>

### <span data-ttu-id="07261-132">System. Object</span><span class="sxs-lookup"><span data-stu-id="07261-132">System.Object</span></span>

## <span data-ttu-id="07261-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="07261-133">NOTES</span></span>

## <span data-ttu-id="07261-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="07261-134">RELATED LINKS</span></span>

[<span data-ttu-id="07261-135">Get-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="07261-135">Get-AzureRmLogicApp</span></span>](./Get-AzureRmLogicApp.md)


