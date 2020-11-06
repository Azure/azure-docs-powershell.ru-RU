---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoorrulegroupoverrideobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorRuleGroupOverrideObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorRuleGroupOverrideObject.md
ms.openlocfilehash: 02253a59a7f05bfdecd8147325575605334f13ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93556639"
---
# <span data-ttu-id="fca1b-101">New-AzureRmFrontDoorRuleGroupOverrideObject</span><span class="sxs-lookup"><span data-stu-id="fca1b-101">New-AzureRmFrontDoorRuleGroupOverrideObject</span></span>

## <span data-ttu-id="fca1b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fca1b-102">SYNOPSIS</span></span>
<span data-ttu-id="fca1b-103">Создание объекта RuleGroupOverride для создания политики WAF</span><span class="sxs-lookup"><span data-stu-id="fca1b-103">Create RuleGroupOverride Object for WAF policy creation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fca1b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fca1b-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorRuleGroupOverrideObject -Override <PSRuleGroupOverride> -Action <PSAction>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fca1b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fca1b-105">DESCRIPTION</span></span>
<span data-ttu-id="fca1b-106">Создание объекта RuleGroupOverride для создания политики WAF</span><span class="sxs-lookup"><span data-stu-id="fca1b-106">Create RuleGroupOverride Object for WAF policy creation</span></span>

## <span data-ttu-id="fca1b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fca1b-107">EXAMPLES</span></span>

### <span data-ttu-id="fca1b-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fca1b-108">Example 1</span></span>
```powershell
PS C:\>  New-AzureRmFrontDoorRuleGroupOverrideObject -Override SqlInjection -Action Block

Action RuleGroupOverride
------ -----------------
 Block      SqlInjection
```

<span data-ttu-id="fca1b-109">Создание объекта RuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="fca1b-109">Create a RuleGroupOverride Object</span></span>

## <span data-ttu-id="fca1b-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fca1b-110">PARAMETERS</span></span>

### <span data-ttu-id="fca1b-111">-Action (действие)</span><span class="sxs-lookup"><span data-stu-id="fca1b-111">-Action</span></span>
<span data-ttu-id="fca1b-112">Тип действий.</span><span class="sxs-lookup"><span data-stu-id="fca1b-112">Type of Actions.</span></span>
<span data-ttu-id="fca1b-113">Возможные значения: "разрешить", "блок", "журнал"</span><span class="sxs-lookup"><span data-stu-id="fca1b-113">Possible values include: 'Allow', 'Block', 'Log'</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSAction
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Block, Log

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fca1b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fca1b-114">-DefaultProfile</span></span>
<span data-ttu-id="fca1b-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fca1b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fca1b-116">-Override</span><span class="sxs-lookup"><span data-stu-id="fca1b-116">-Override</span></span>
<span data-ttu-id="fca1b-117">Описывает overrideruleGroup.</span><span class="sxs-lookup"><span data-stu-id="fca1b-117">Describes overrideruleGroup.</span></span>
<span data-ttu-id="fca1b-118">Возможные значения: "SqlInjection", "XSS"</span><span class="sxs-lookup"><span data-stu-id="fca1b-118">Possible values include: 'SqlInjection', 'XSS'</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRuleGroupOverride
Parameter Sets: (All)
Aliases:
Accepted values: SqlInjection, XSS

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fca1b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fca1b-119">CommonParameters</span></span>
<span data-ttu-id="fca1b-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fca1b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fca1b-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fca1b-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fca1b-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fca1b-122">INPUTS</span></span>

### <span data-ttu-id="fca1b-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="fca1b-123">None</span></span>

## <span data-ttu-id="fca1b-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fca1b-124">OUTPUTS</span></span>

### <span data-ttu-id="fca1b-125">Microsoft. Azure. Commands. FrontDoor. Models. PSAzureRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="fca1b-125">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureRuleGroupOverride</span></span>

## <span data-ttu-id="fca1b-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="fca1b-126">NOTES</span></span>

## <span data-ttu-id="fca1b-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fca1b-127">RELATED LINKS</span></span>

[<span data-ttu-id="fca1b-128">New-AzureRmFrontDoorManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="fca1b-128">New-AzureRmFrontDoorManagedRuleObject</span></span>](./New-AzureRmFrontDoorManagedRuleObject.md)
