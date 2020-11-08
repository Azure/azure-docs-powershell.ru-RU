---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplicationGroup.md
ms.openlocfilehash: 0dfbcabcb1869457e29d6c16c861c0743f50dc5a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236732"
---
# <span data-ttu-id="faa17-101">New-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="faa17-101">New-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="faa17-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="faa17-102">SYNOPSIS</span></span>
<span data-ttu-id="faa17-103">Создание или обновление applicationGroup.</span><span class="sxs-lookup"><span data-stu-id="faa17-103">Create or update an applicationGroup.</span></span>

## <span data-ttu-id="faa17-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="faa17-104">SYNTAX</span></span>

```
New-AzWvdApplicationGroup -Name <String> -ResourceGroupName <String>
 -ApplicationGroupType <ApplicationGroupType> -HostPoolArmPath <String> -Location <String>
 [-SubscriptionId <String>] [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="faa17-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="faa17-105">DESCRIPTION</span></span>
<span data-ttu-id="faa17-106">Создание или обновление applicationGroup.</span><span class="sxs-lookup"><span data-stu-id="faa17-106">Create or update an applicationGroup.</span></span>

## <span data-ttu-id="faa17-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="faa17-107">EXAMPLES</span></span>

### <span data-ttu-id="faa17-108">Пример 1: создание виртуального рабочего стола Windows ApplicationGroup по имени</span><span class="sxs-lookup"><span data-stu-id="faa17-108">Example 1: Create a Windows Virtual Desktop ApplicationGroup by name</span></span>
```powershell
PS C:\> New-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName `
                            -Name ApplicationGroupName `
                            -Location 'eastus' `
                            -FriendlyName 'Friendly Name' `
                            -Description 'Description' `
                            -HostPoolArmPath '/subscriptions/SubscriptionId/resourcegroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/hostPools/HostPoolName' `
                            -ApplicationGroupType 'RemoteApp'

Location   Name                 Type
--------   ----                 ----
eastus     ApplicationGroupName Microsoft.DesktopVirtualization/applicationgroups
```

<span data-ttu-id="faa17-109">Эта команда создает ApplicationGroup виртуальных рабочих столов Windows в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="faa17-109">This command creates a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

### <span data-ttu-id="faa17-110">Пример 2: создание виртуального рабочего стола Windows ApplicationGroup по имени</span><span class="sxs-lookup"><span data-stu-id="faa17-110">Example 2: Create a Windows Virtual Desktop ApplicationGroup by name</span></span>
```powershell
PS C:\> New-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName `
                            -Name ApplicationGroupName `
                            -Location 'eastus' `
                            -FriendlyName 'Friendly Name' `
                            -Description 'Description' `
                            -HostPoolArmPath '/subscriptions/SubscriptionId/resourcegroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/hostPools/HostPoolName' `
                            -ApplicationGroupType 'Desktop'

Location   Name                 Type
--------   ----                 ----
eastus     ApplicationGroupName Microsoft.DesktopVirtualization/applicationgroups
```

<span data-ttu-id="faa17-111">Эта команда создает ApplicationGroup виртуальных рабочих столов Windows в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="faa17-111">This command creates a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

## <span data-ttu-id="faa17-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="faa17-112">PARAMETERS</span></span>

### <span data-ttu-id="faa17-113">-ApplicationGroupType</span><span class="sxs-lookup"><span data-stu-id="faa17-113">-ApplicationGroupType</span></span>
<span data-ttu-id="faa17-114">Тип ресурса ApplicationGroup.</span><span class="sxs-lookup"><span data-stu-id="faa17-114">Resource Type of ApplicationGroup.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.ApplicationGroupType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="faa17-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="faa17-115">-DefaultProfile</span></span>
<span data-ttu-id="faa17-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="faa17-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="faa17-117">-Описание</span><span class="sxs-lookup"><span data-stu-id="faa17-117">-Description</span></span>
<span data-ttu-id="faa17-118">Описание ApplicationGroup.</span><span class="sxs-lookup"><span data-stu-id="faa17-118">Description of ApplicationGroup.</span></span>

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

### <span data-ttu-id="faa17-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="faa17-119">-FriendlyName</span></span>
<span data-ttu-id="faa17-120">Понятное имя ApplicationGroup.</span><span class="sxs-lookup"><span data-stu-id="faa17-120">Friendly name of ApplicationGroup.</span></span>

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

### <span data-ttu-id="faa17-121">-HostPoolArmPath</span><span class="sxs-lookup"><span data-stu-id="faa17-121">-HostPoolArmPath</span></span>
<span data-ttu-id="faa17-122">HostPool путь к ApplicationGroup.</span><span class="sxs-lookup"><span data-stu-id="faa17-122">HostPool arm path of ApplicationGroup.</span></span>

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

### <span data-ttu-id="faa17-123">-Location</span><span class="sxs-lookup"><span data-stu-id="faa17-123">-Location</span></span>
<span data-ttu-id="faa17-124">Географическое расположение, в котором находится ресурс</span><span class="sxs-lookup"><span data-stu-id="faa17-124">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="faa17-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="faa17-125">-Name</span></span>
<span data-ttu-id="faa17-126">Имя группы приложения.</span><span class="sxs-lookup"><span data-stu-id="faa17-126">The name of the application group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="faa17-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="faa17-127">-ResourceGroupName</span></span>
<span data-ttu-id="faa17-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="faa17-128">The name of the resource group.</span></span>
<span data-ttu-id="faa17-129">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="faa17-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="faa17-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="faa17-130">-SubscriptionId</span></span>
<span data-ttu-id="faa17-131">Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="faa17-131">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="faa17-132">-Тег</span><span class="sxs-lookup"><span data-stu-id="faa17-132">-Tag</span></span>
<span data-ttu-id="faa17-133">Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="faa17-133">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="faa17-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="faa17-134">-Confirm</span></span>
<span data-ttu-id="faa17-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="faa17-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="faa17-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="faa17-136">-WhatIf</span></span>
<span data-ttu-id="faa17-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="faa17-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="faa17-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="faa17-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="faa17-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="faa17-139">CommonParameters</span></span>
<span data-ttu-id="faa17-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="faa17-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="faa17-141">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="faa17-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="faa17-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="faa17-142">INPUTS</span></span>

## <span data-ttu-id="faa17-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="faa17-143">OUTPUTS</span></span>

### <span data-ttu-id="faa17-144">Microsoft. Azure. PowerShell. командлеты. DesktopVirtualization. Models. Api20191210Preview. IApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="faa17-144">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IApplicationGroup</span></span>

## <span data-ttu-id="faa17-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="faa17-145">NOTES</span></span>

<span data-ttu-id="faa17-146">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="faa17-146">ALIASES</span></span>

## <span data-ttu-id="faa17-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="faa17-147">RELATED LINKS</span></span>

