---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplicationGroup.md
ms.openlocfilehash: bbbdd1a3cd324a57d4889e3afe01f387bc5b478e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98507574"
---
# <span data-ttu-id="8683d-101">New-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="8683d-101">New-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="8683d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8683d-102">SYNOPSIS</span></span>
<span data-ttu-id="8683d-103">Создайте или обновйте приложениеGroup.</span><span class="sxs-lookup"><span data-stu-id="8683d-103">Create or update an applicationGroup.</span></span>

## <span data-ttu-id="8683d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8683d-104">SYNTAX</span></span>

```
New-AzWvdApplicationGroup -Name <String> -ResourceGroupName <String>
 -ApplicationGroupType <ApplicationGroupType> -HostPoolArmPath <String> -Location <String>
 [-SubscriptionId <String>] [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8683d-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8683d-105">DESCRIPTION</span></span>
<span data-ttu-id="8683d-106">Создание или обновление группы приложений.</span><span class="sxs-lookup"><span data-stu-id="8683d-106">Create or update an applicationGroup.</span></span>

## <span data-ttu-id="8683d-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8683d-107">EXAMPLES</span></span>

### <span data-ttu-id="8683d-108">Пример 1. Создание группы приложений виртуального рабочего стола Windows по имени</span><span class="sxs-lookup"><span data-stu-id="8683d-108">Example 1: Create a Windows Virtual Desktop ApplicationGroup by name</span></span>
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

<span data-ttu-id="8683d-109">Эта команда создает группу приложений Виртуального рабочего стола Windows в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8683d-109">This command creates a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

### <span data-ttu-id="8683d-110">Пример 2. Создание группы приложений виртуального рабочего стола Windows по имени</span><span class="sxs-lookup"><span data-stu-id="8683d-110">Example 2: Create a Windows Virtual Desktop ApplicationGroup by name</span></span>
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

<span data-ttu-id="8683d-111">Эта команда создает группу приложений Виртуального рабочего стола Windows в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8683d-111">This command creates a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

## <span data-ttu-id="8683d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8683d-112">PARAMETERS</span></span>

### <span data-ttu-id="8683d-113">-ApplicationGroupType</span><span class="sxs-lookup"><span data-stu-id="8683d-113">-ApplicationGroupType</span></span>
<span data-ttu-id="8683d-114">Тип ресурса ApplicationGroup.</span><span class="sxs-lookup"><span data-stu-id="8683d-114">Resource Type of ApplicationGroup.</span></span>

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

### <span data-ttu-id="8683d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8683d-115">-DefaultProfile</span></span>
<span data-ttu-id="8683d-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8683d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8683d-117">-Description</span><span class="sxs-lookup"><span data-stu-id="8683d-117">-Description</span></span>
<span data-ttu-id="8683d-118">Описание ApplicationGroup.</span><span class="sxs-lookup"><span data-stu-id="8683d-118">Description of ApplicationGroup.</span></span>

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

### <span data-ttu-id="8683d-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="8683d-119">-FriendlyName</span></span>
<span data-ttu-id="8683d-120">Имя ApplicationGroup.</span><span class="sxs-lookup"><span data-stu-id="8683d-120">Friendly name of ApplicationGroup.</span></span>

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

### <span data-ttu-id="8683d-121">-HostPoolArmPath</span><span class="sxs-lookup"><span data-stu-id="8683d-121">-HostPoolArmPath</span></span>
<span data-ttu-id="8683d-122">Путь к armpool хоста ApplicationGroup.</span><span class="sxs-lookup"><span data-stu-id="8683d-122">HostPool arm path of ApplicationGroup.</span></span>

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

### <span data-ttu-id="8683d-123">-Location</span><span class="sxs-lookup"><span data-stu-id="8683d-123">-Location</span></span>
<span data-ttu-id="8683d-124">Географическое расположение ресурса</span><span class="sxs-lookup"><span data-stu-id="8683d-124">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="8683d-125">-Name</span><span class="sxs-lookup"><span data-stu-id="8683d-125">-Name</span></span>
<span data-ttu-id="8683d-126">Имя группы приложений</span><span class="sxs-lookup"><span data-stu-id="8683d-126">The name of the application group</span></span>

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

### <span data-ttu-id="8683d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8683d-127">-ResourceGroupName</span></span>
<span data-ttu-id="8683d-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8683d-128">The name of the resource group.</span></span>
<span data-ttu-id="8683d-129">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="8683d-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="8683d-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8683d-130">-SubscriptionId</span></span>
<span data-ttu-id="8683d-131">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="8683d-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="8683d-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="8683d-132">-Tag</span></span>
<span data-ttu-id="8683d-133">Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8683d-133">Resource tags.</span></span>

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

### <span data-ttu-id="8683d-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8683d-134">-Confirm</span></span>
<span data-ttu-id="8683d-135">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8683d-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8683d-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8683d-136">-WhatIf</span></span>
<span data-ttu-id="8683d-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8683d-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8683d-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="8683d-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8683d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8683d-139">CommonParameters</span></span>
<span data-ttu-id="8683d-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8683d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8683d-141">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8683d-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8683d-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8683d-142">INPUTS</span></span>

## <span data-ttu-id="8683d-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8683d-143">OUTPUTS</span></span>

### <span data-ttu-id="8683d-144">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="8683d-144">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplicationGroup</span></span>

## <span data-ttu-id="8683d-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8683d-145">NOTES</span></span>

<span data-ttu-id="8683d-146">ALIASES</span><span class="sxs-lookup"><span data-stu-id="8683d-146">ALIASES</span></span>

## <span data-ttu-id="8683d-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8683d-147">RELATED LINKS</span></span>

