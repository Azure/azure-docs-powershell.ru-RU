---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/set-azdataboxedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeShare.md
ms.openlocfilehash: 8c31f5f97b723db63253165e21d2abea220f18d3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971288"
---
# <span data-ttu-id="61eaa-101">Set-AzDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="61eaa-101">Set-AzDataBoxEdgeShare</span></span>

## <span data-ttu-id="61eaa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61eaa-102">SYNOPSIS</span></span>
<span data-ttu-id="61eaa-103">Обновляет обойму для устройства.</span><span class="sxs-lookup"><span data-stu-id="61eaa-103">Updates the share for a device.</span></span>

## <span data-ttu-id="61eaa-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="61eaa-104">SYNTAX</span></span>

### <span data-ttu-id="61eaa-105">SmbParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="61eaa-105">SmbParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -UserAccessRight <Hashtable[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="61eaa-106">UpdateByResourceIdSmbParameterSet</span><span class="sxs-lookup"><span data-stu-id="61eaa-106">UpdateByResourceIdSmbParameterSet</span></span>
```
Set-AzDataBoxEdgeShare -ResourceId <String> -UserAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61eaa-107">UpdateByResourceIdNfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="61eaa-107">UpdateByResourceIdNfsParameterSet</span></span>
```
Set-AzDataBoxEdgeShare -ResourceId <String> -ClientAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61eaa-108">UpdateByInputObjectSmbParameterSet</span><span class="sxs-lookup"><span data-stu-id="61eaa-108">UpdateByInputObjectSmbParameterSet</span></span>
```
Set-AzDataBoxEdgeShare -InputObject <PSDataBoxEdgeShare> -UserAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61eaa-109">UpdateByInputObjectNfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="61eaa-109">UpdateByInputObjectNfsParameterSet</span></span>
```
Set-AzDataBoxEdgeShare -InputObject <PSDataBoxEdgeShare> -ClientAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61eaa-110">NfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="61eaa-110">NfsParameterSet</span></span>
```
Set-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -ClientAccessRight <Hashtable[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="61eaa-111">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="61eaa-111">DESCRIPTION</span></span>
<span data-ttu-id="61eaa-112">Это **set-AzDataBoxEdgeShare** заменит права на доступ</span><span class="sxs-lookup"><span data-stu-id="61eaa-112">This **Set-AzDataBoxEdgeShare** will replace the access rights</span></span>

## <span data-ttu-id="61eaa-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="61eaa-113">EXAMPLES</span></span>

### <span data-ttu-id="61eaa-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="61eaa-114">Example 1</span></span>
```powershell
PS C:\> $AccessRights = @(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})
PS C:\> Set-AzDataBoxEdgeShare -ResourceGroupName resource-group-name -ClientAccessRight $AccessRights
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-2    NFS        Cloud            PageBlob         resource-group-name   storage-account-name
## $ClientAccessRights = @(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})
## Possible values for AccessRight options are 'NoAccess', 'ReadOnly', 'ReadWrite'
```

### <span data-ttu-id="61eaa-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="61eaa-115">Example 2</span></span>
```powershell
PS C:\> $AccessRights = @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})
PS C:\> Set-AzDataBoxEdgeShare -ResourceGroupName resource-group-name -UserAccessRight $AccessRights
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-1    SMB        Cloud            PageBlob         resource-group-name   storage-account-name
## $UserAccessRights = @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})
## Possible values for AccessRight are 'Change', 'Read', 'Custom'
```

## <span data-ttu-id="61eaa-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="61eaa-116">PARAMETERS</span></span>

### <span data-ttu-id="61eaa-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="61eaa-117">-AsJob</span></span>
<span data-ttu-id="61eaa-118">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="61eaa-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="61eaa-119">-ClientAccessRight</span><span class="sxs-lookup"><span data-stu-id="61eaa-119">-ClientAccessRight</span></span>
<span data-ttu-id="61eaa-120">Read/Write Access for clientIds, for ex:@(@{"ClientId"="192.168.10.10";" AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";" AccessRight"="ReadOnly"})</span><span class="sxs-lookup"><span data-stu-id="61eaa-120">Read/Write Access for clientIds, For ex:@(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: UpdateByResourceIdNfsParameterSet, UpdateByInputObjectNfsParameterSet, NfsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61eaa-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61eaa-121">-DefaultProfile</span></span>
<span data-ttu-id="61eaa-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="61eaa-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61eaa-123">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="61eaa-123">-DeviceName</span></span>
<span data-ttu-id="61eaa-124">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="61eaa-124">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: SmbParameterSet, NfsParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61eaa-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="61eaa-125">-InputObject</span></span>
<span data-ttu-id="61eaa-126">Объект Input</span><span class="sxs-lookup"><span data-stu-id="61eaa-126">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare
Parameter Sets: UpdateByInputObjectSmbParameterSet, UpdateByInputObjectNfsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="61eaa-127">-Name</span><span class="sxs-lookup"><span data-stu-id="61eaa-127">-Name</span></span>
<span data-ttu-id="61eaa-128">Название ресурса</span><span class="sxs-lookup"><span data-stu-id="61eaa-128">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: SmbParameterSet, NfsParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61eaa-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61eaa-129">-ResourceGroupName</span></span>
<span data-ttu-id="61eaa-130">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="61eaa-130">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: SmbParameterSet, NfsParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61eaa-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="61eaa-131">-ResourceId</span></span>
<span data-ttu-id="61eaa-132">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="61eaa-132">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdSmbParameterSet, UpdateByResourceIdNfsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61eaa-133">-UserAccessRight</span><span class="sxs-lookup"><span data-stu-id="61eaa-133">-UserAccessRight</span></span>
<span data-ttu-id="61eaa-134">предоставить доступ прямо вместе с существующими именами пользователей для доступа к типам "Общий доступ К SMB", например: @(@{"Имя пользователя"="имя пользователя-1";" AccessRight"="Read"}, @{"Username"="user-name-2";" AccessRight"="Read"}, @{"Username"="user-name-3";" AccessRight"="Custom"})</span><span class="sxs-lookup"><span data-stu-id="61eaa-134">provide access right along with existing usernames to access SMB Share types, For ex: @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: SmbParameterSet, UpdateByResourceIdSmbParameterSet, UpdateByInputObjectSmbParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61eaa-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="61eaa-135">-Confirm</span></span>
<span data-ttu-id="61eaa-136">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61eaa-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61eaa-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61eaa-137">-WhatIf</span></span>
<span data-ttu-id="61eaa-138">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61eaa-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="61eaa-139">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="61eaa-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61eaa-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61eaa-140">CommonParameters</span></span>
<span data-ttu-id="61eaa-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61eaa-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61eaa-142">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="61eaa-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61eaa-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="61eaa-143">INPUTS</span></span>

### <span data-ttu-id="61eaa-144">System.String</span><span class="sxs-lookup"><span data-stu-id="61eaa-144">System.String</span></span>

### <span data-ttu-id="61eaa-145">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDAtaBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="61eaa-145">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span></span>

## <span data-ttu-id="61eaa-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="61eaa-146">OUTPUTS</span></span>

### <span data-ttu-id="61eaa-147">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDAtaBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="61eaa-147">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span></span>

## <span data-ttu-id="61eaa-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="61eaa-148">NOTES</span></span>

## <span data-ttu-id="61eaa-149">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="61eaa-149">RELATED LINKS</span></span>
