---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/set-azdataboxedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeShare.md
ms.openlocfilehash: 8bef754d7d9020193e4694953222a6579341c9ed
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94314162"
---
# <span data-ttu-id="92a12-101">Set-AzDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="92a12-101">Set-AzDataBoxEdgeShare</span></span>

## <span data-ttu-id="92a12-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="92a12-102">SYNOPSIS</span></span>
<span data-ttu-id="92a12-103">Обновление общего доступа для устройства.</span><span class="sxs-lookup"><span data-stu-id="92a12-103">Updates the share for a device.</span></span>

## <span data-ttu-id="92a12-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="92a12-104">SYNTAX</span></span>

### <span data-ttu-id="92a12-105">SmbParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="92a12-105">SmbParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -UserAccessRight <Hashtable[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="92a12-106">UpdateByResourceIdSmbParameterSet</span><span class="sxs-lookup"><span data-stu-id="92a12-106">UpdateByResourceIdSmbParameterSet</span></span>
```
Set-AzDataBoxEdgeShare -ResourceId <String> -UserAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92a12-107">UpdateByResourceIdNfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="92a12-107">UpdateByResourceIdNfsParameterSet</span></span>
```
Set-AzDataBoxEdgeShare -ResourceId <String> -ClientAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92a12-108">UpdateByInputObjectSmbParameterSet</span><span class="sxs-lookup"><span data-stu-id="92a12-108">UpdateByInputObjectSmbParameterSet</span></span>
```
Set-AzDataBoxEdgeShare -InputObject <PSDataBoxEdgeShare> -UserAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92a12-109">UpdateByInputObjectNfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="92a12-109">UpdateByInputObjectNfsParameterSet</span></span>
```
Set-AzDataBoxEdgeShare -InputObject <PSDataBoxEdgeShare> -ClientAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92a12-110">NfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="92a12-110">NfsParameterSet</span></span>
```
Set-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -ClientAccessRight <Hashtable[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="92a12-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="92a12-111">DESCRIPTION</span></span>
<span data-ttu-id="92a12-112">Этот **Set-AzDataBoxEdgeShare** заменит права доступа</span><span class="sxs-lookup"><span data-stu-id="92a12-112">This **Set-AzDataBoxEdgeShare** will replace the access rights</span></span>

## <span data-ttu-id="92a12-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="92a12-113">EXAMPLES</span></span>

### <span data-ttu-id="92a12-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="92a12-114">Example 1</span></span>
```powershell
PS C:\> $AccessRights = @(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})
PS C:\> Set-AzDataBoxEdgeShare -ResourceGroupName resource-group-name -ClientAccessRight $AccessRights
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-2    NFS        Cloud            PageBlob         resource-group-name   storage-account-name
## $ClientAccessRights = @(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})
## Possible values for AccessRight options are 'NoAccess', 'ReadOnly', 'ReadWrite'
```

### <span data-ttu-id="92a12-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="92a12-115">Example 2</span></span>
```powershell
PS C:\> $AccessRights = @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})
PS C:\> Set-AzDataBoxEdgeShare -ResourceGroupName resource-group-name -UserAccessRight $AccessRights
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-1    SMB        Cloud            PageBlob         resource-group-name   storage-account-name
## $UserAccessRights = @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})
## Possible values for AccessRight are 'Change', 'Read', 'Custom'
```

## <span data-ttu-id="92a12-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="92a12-116">PARAMETERS</span></span>

### <span data-ttu-id="92a12-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="92a12-117">-AsJob</span></span>
<span data-ttu-id="92a12-118">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="92a12-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="92a12-119">-ClientAccessRight</span><span class="sxs-lookup"><span data-stu-id="92a12-119">-ClientAccessRight</span></span>
<span data-ttu-id="92a12-120">Доступ для чтения и записи для clientId, для ex: @ (@ {"ClientId" = "192.168.10.10"; " AccessRight "=" недоступен "}, @ {" ClientId "=" 192.168.10.11 ";" AccessRight "=" только для чтения "})</span><span class="sxs-lookup"><span data-stu-id="92a12-120">Read/Write Access for clientIds, For ex:@(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})</span></span>

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

### <span data-ttu-id="92a12-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92a12-121">-DefaultProfile</span></span>
<span data-ttu-id="92a12-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="92a12-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92a12-123">-Имя_устройства</span><span class="sxs-lookup"><span data-stu-id="92a12-123">-DeviceName</span></span>
<span data-ttu-id="92a12-124">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="92a12-124">Device Name</span></span>

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

### <span data-ttu-id="92a12-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="92a12-125">-InputObject</span></span>
<span data-ttu-id="92a12-126">Объект input</span><span class="sxs-lookup"><span data-stu-id="92a12-126">Input Object</span></span>

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

### <span data-ttu-id="92a12-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="92a12-127">-Name</span></span>
<span data-ttu-id="92a12-128">Название ресурса</span><span class="sxs-lookup"><span data-stu-id="92a12-128">Resource Name</span></span>

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

### <span data-ttu-id="92a12-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92a12-129">-ResourceGroupName</span></span>
<span data-ttu-id="92a12-130">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="92a12-130">Resource Group Name</span></span>

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

### <span data-ttu-id="92a12-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="92a12-131">-ResourceId</span></span>
<span data-ttu-id="92a12-132">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="92a12-132">Azure ResourceId</span></span>

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

### <span data-ttu-id="92a12-133">-UserAccessRight</span><span class="sxs-lookup"><span data-stu-id="92a12-133">-UserAccessRight</span></span>
<span data-ttu-id="92a12-134">Предоставьте право доступа вместе с существующими именами пользователей для доступа к типам общего доступа к SMB, например: @ (@ {"Username" = "User-Name-1"; " AccessRight "=" Read "}, @ {" ИмяПользователя "=" User-Name-2 ";" AccessRight "=" Read "}, @ {" ИмяПользователя "=" User-Name-3 ";" AccessRight "=" Custom "})</span><span class="sxs-lookup"><span data-stu-id="92a12-134">provide access right along with existing usernames to access SMB Share types, For ex: @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})</span></span>

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

### <span data-ttu-id="92a12-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="92a12-135">-Confirm</span></span>
<span data-ttu-id="92a12-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="92a12-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92a12-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92a12-137">-WhatIf</span></span>
<span data-ttu-id="92a12-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="92a12-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="92a12-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="92a12-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92a12-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92a12-140">CommonParameters</span></span>
<span data-ttu-id="92a12-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="92a12-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92a12-142">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="92a12-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92a12-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="92a12-143">INPUTS</span></span>

### <span data-ttu-id="92a12-144">System. String</span><span class="sxs-lookup"><span data-stu-id="92a12-144">System.String</span></span>

### <span data-ttu-id="92a12-145">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="92a12-145">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span></span>

## <span data-ttu-id="92a12-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="92a12-146">OUTPUTS</span></span>

### <span data-ttu-id="92a12-147">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="92a12-147">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span></span>

## <span data-ttu-id="92a12-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="92a12-148">NOTES</span></span>

## <span data-ttu-id="92a12-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="92a12-149">RELATED LINKS</span></span>
