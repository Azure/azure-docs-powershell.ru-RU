---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoormanagedruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorManagedRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorManagedRuleObject.md
ms.openlocfilehash: 236cb9ff263f97ae52ea5d3226f4defec00c662a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732930"
---
# <span data-ttu-id="13d96-101">New-AzureRmFrontDoorManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="13d96-101">New-AzureRmFrontDoorManagedRuleObject</span></span>

## <span data-ttu-id="13d96-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="13d96-102">SYNOPSIS</span></span>
<span data-ttu-id="13d96-103">Создание объекта ManagedRule для создания политики WAF</span><span class="sxs-lookup"><span data-stu-id="13d96-103">Create ManagedRule Object for WAF policy creation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="13d96-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="13d96-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorManagedRuleObject -Priority <Int32> [-Version <String>]
 [-RuleGroupOverride <PSAzureRuleGroupOverride[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="13d96-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="13d96-105">DESCRIPTION</span></span>
<span data-ttu-id="13d96-106">Создание объекта ManagedRule для создания политики WAF</span><span class="sxs-lookup"><span data-stu-id="13d96-106">Create ManagedRule Object for WAF policy creation</span></span>

## <span data-ttu-id="13d96-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="13d96-107">EXAMPLES</span></span>

### <span data-ttu-id="13d96-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="13d96-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmFrontDoor
ManagedRuleObject -Priority 1 -Version 0 -RuleGroupOverride $override1

RuleGroupOverrides                                                   Priority Version
------------------                                                   -------- -------
{Microsoft.Azure.Commands.FrontDoor.Models.PSAzureRuleGroupOverride}        1 0
```

<span data-ttu-id="13d96-109">Создание объекта ManagedRule</span><span class="sxs-lookup"><span data-stu-id="13d96-109">Create a ManagedRule Object</span></span>

## <span data-ttu-id="13d96-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="13d96-110">PARAMETERS</span></span>

### <span data-ttu-id="13d96-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13d96-111">-DefaultProfile</span></span>
<span data-ttu-id="13d96-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="13d96-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13d96-113">-Priority (приоритет)</span><span class="sxs-lookup"><span data-stu-id="13d96-113">-Priority</span></span>
<span data-ttu-id="13d96-114">Описывает приоритет правила.</span><span class="sxs-lookup"><span data-stu-id="13d96-114">Describes priority of the rule</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13d96-115">-RuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="13d96-115">-RuleGroupOverride</span></span>
<span data-ttu-id="13d96-116">Список конфигурации переопределения поставщика управляемых служб Azure</span><span class="sxs-lookup"><span data-stu-id="13d96-116">List of azure managed provider override configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSAzureRuleGroupOverride[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13d96-117">-Version</span><span class="sxs-lookup"><span data-stu-id="13d96-117">-Version</span></span>
<span data-ttu-id="13d96-118">Версия набора правил</span><span class="sxs-lookup"><span data-stu-id="13d96-118">Version of the ruleset</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13d96-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13d96-119">CommonParameters</span></span>
<span data-ttu-id="13d96-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="13d96-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13d96-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13d96-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13d96-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="13d96-122">INPUTS</span></span>

### <span data-ttu-id="13d96-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="13d96-123">None</span></span>

## <span data-ttu-id="13d96-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="13d96-124">OUTPUTS</span></span>

### <span data-ttu-id="13d96-125">Microsoft. Azure. Commands. FrontDoor. Models. PSAzureManagedRule</span><span class="sxs-lookup"><span data-stu-id="13d96-125">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule</span></span>

## <span data-ttu-id="13d96-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="13d96-126">NOTES</span></span>

## <span data-ttu-id="13d96-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="13d96-127">RELATED LINKS</span></span>

<span data-ttu-id="13d96-128">[New-AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md) 
 [Set-AzureRmFrontDoorFireWallPolicy](./Set-AzureRmFrontDoorFireWallPolicy.md) 
 [New-AzureRmFrontDoorRuleGroupOverrideObject](./Set-AzureRmFrontDoorRuleGroupOverrideObject.md)</span><span class="sxs-lookup"><span data-stu-id="13d96-128">[New-AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md)
[Set-AzureRmFrontDoorFireWallPolicy](./Set-AzureRmFrontDoorFireWallPolicy.md)
[New-AzureRmFrontDoorRuleGroupOverrideObject](./Set-AzureRmFrontDoorRuleGroupOverrideObject.md)</span></span>
