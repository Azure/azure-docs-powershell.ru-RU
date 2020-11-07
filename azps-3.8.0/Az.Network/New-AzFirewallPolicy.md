---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicy.md
ms.openlocfilehash: 5c432224891de6c2fcadc42ae308e9607bc3e432
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93911732"
---
# <span data-ttu-id="92e1a-101">New-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="92e1a-101">New-AzFirewallPolicy</span></span>

## <span data-ttu-id="92e1a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="92e1a-102">SYNOPSIS</span></span>
<span data-ttu-id="92e1a-103">Создание новой политики брандмауэра Azure</span><span class="sxs-lookup"><span data-stu-id="92e1a-103">Creates a new Azure Firewall Policy</span></span>

## <span data-ttu-id="92e1a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="92e1a-104">SYNTAX</span></span>

```
New-AzFirewallPolicy -Name <String> -ResourceGroupName <String> -Location <String> [-ThreatIntelMode <String>]
 [-BasePolicy <String>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92e1a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="92e1a-105">DESCRIPTION</span></span>
<span data-ttu-id="92e1a-106">Командлет **New-AzFirewallPolicy** создает политику брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="92e1a-106">The **New-AzFirewallPolicy** cmdlet creates an Azure Firewall Policy.</span></span>

## <span data-ttu-id="92e1a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="92e1a-107">EXAMPLES</span></span>

### <span data-ttu-id="92e1a-108">1. Создание пустой политики</span><span class="sxs-lookup"><span data-stu-id="92e1a-108">1. Create an empty policy</span></span>
```powershell
PS C:\> New-AzFirewallPolicy -Name fp1 -ResourceGroupName TestRg
```

<span data-ttu-id="92e1a-109">В этом примере создается политика брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="92e1a-109">This example creates an azure firewall policy</span></span>

### <span data-ttu-id="92e1a-110">2. Создание пустой политики с помощью режима ThreatIntel</span><span class="sxs-lookup"><span data-stu-id="92e1a-110">2. Create an empty policy with ThreatIntel Mode</span></span>
```powershell
PS C:\> New-AzFirewallPolicy -Name fp1 -ResourceGroupName TestRg -ThreatIntelMode "Deny"
```

<span data-ttu-id="92e1a-111">В этом примере создается политика брандмауэра Azure с режимом угроз Intel</span><span class="sxs-lookup"><span data-stu-id="92e1a-111">This example creates an azure firewall policy with a threat intel mode</span></span>

## <span data-ttu-id="92e1a-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="92e1a-112">PARAMETERS</span></span>

### <span data-ttu-id="92e1a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="92e1a-113">-AsJob</span></span>
<span data-ttu-id="92e1a-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="92e1a-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92e1a-115">-BasePolicy</span><span class="sxs-lookup"><span data-stu-id="92e1a-115">-BasePolicy</span></span>
<span data-ttu-id="92e1a-116">Режим работы для логики операций с угрозами.</span><span class="sxs-lookup"><span data-stu-id="92e1a-116">The operation mode for Threat Intelligence.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92e1a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92e1a-117">-DefaultProfile</span></span>
<span data-ttu-id="92e1a-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="92e1a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92e1a-119">-Force</span><span class="sxs-lookup"><span data-stu-id="92e1a-119">-Force</span></span>
<span data-ttu-id="92e1a-120">Не запрашивать подтверждение, если вы хотите перезаписать ресурс</span><span class="sxs-lookup"><span data-stu-id="92e1a-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92e1a-121">-Location</span><span class="sxs-lookup"><span data-stu-id="92e1a-121">-Location</span></span>
<span data-ttu-id="92e1a-122">поиска.</span><span class="sxs-lookup"><span data-stu-id="92e1a-122">location.</span></span>

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

### <span data-ttu-id="92e1a-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="92e1a-123">-Name</span></span>
<span data-ttu-id="92e1a-124">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="92e1a-124">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92e1a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92e1a-125">-ResourceGroupName</span></span>
<span data-ttu-id="92e1a-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="92e1a-126">The resource group name.</span></span>

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

### <span data-ttu-id="92e1a-127">-Тег</span><span class="sxs-lookup"><span data-stu-id="92e1a-127">-Tag</span></span>
<span data-ttu-id="92e1a-128">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="92e1a-128">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92e1a-129">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="92e1a-129">-ThreatIntelMode</span></span>
<span data-ttu-id="92e1a-130">Режим работы для логики операций с угрозами.</span><span class="sxs-lookup"><span data-stu-id="92e1a-130">The operation mode for Threat Intelligence.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Alert, Deny, Off

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92e1a-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="92e1a-131">-Confirm</span></span>
<span data-ttu-id="92e1a-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="92e1a-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92e1a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92e1a-133">-WhatIf</span></span>
<span data-ttu-id="92e1a-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="92e1a-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92e1a-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="92e1a-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92e1a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92e1a-136">CommonParameters</span></span>
<span data-ttu-id="92e1a-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="92e1a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92e1a-138">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="92e1a-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92e1a-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="92e1a-139">INPUTS</span></span>

### <span data-ttu-id="92e1a-140">System. String</span><span class="sxs-lookup"><span data-stu-id="92e1a-140">System.String</span></span>

### <span data-ttu-id="92e1a-141">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="92e1a-141">System.Collections.Hashtable</span></span>

## <span data-ttu-id="92e1a-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="92e1a-142">OUTPUTS</span></span>

### <span data-ttu-id="92e1a-143">Microsoft. Azure. Commands. Network. Models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="92e1a-143">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="92e1a-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="92e1a-144">NOTES</span></span>

## <span data-ttu-id="92e1a-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="92e1a-145">RELATED LINKS</span></span>
