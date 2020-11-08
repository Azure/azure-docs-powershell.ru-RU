---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesVolume.md
ms.openlocfilehash: c28b53fcd9b65198554f34cacd6f628d977e703a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248383"
---
# <span data-ttu-id="6362f-101">Update-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="6362f-101">Update-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="6362f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6362f-102">SYNOPSIS</span></span>
<span data-ttu-id="6362f-103">Обновляет том Azure NetApp Files (ANF) в соответствии с необязательными модификаторами.</span><span class="sxs-lookup"><span data-stu-id="6362f-103">Updates an Azure NetApp Files (ANF) volume according to the optional modifiers provided.</span></span>

## <span data-ttu-id="6362f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6362f-104">SYNTAX</span></span>

### <span data-ttu-id="6362f-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6362f-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesVolume -ResourceGroupName <String> -Location <String> -AccountName <String>
 -PoolName <String> -Name <String> [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6362f-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6362f-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesVolume -Name <String> [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Tag <Hashtable>] -PoolObject <PSNetAppFilesPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6362f-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6362f-107">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesVolume [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Tag <Hashtable>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6362f-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6362f-108">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesVolume [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Tag <Hashtable>] -InputObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6362f-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6362f-109">DESCRIPTION</span></span>
<span data-ttu-id="6362f-110">Командлет **Update-AzNetAppFilesVolume** ОБНОВЛЯЕТ том ANF.</span><span class="sxs-lookup"><span data-stu-id="6362f-110">The **Update-AzNetAppFilesVolume** cmdlet updates an ANF volume.</span></span>

## <span data-ttu-id="6362f-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6362f-111">EXAMPLES</span></span>

### <span data-ttu-id="6362f-112">Пример 1: обновление тома ANF</span><span class="sxs-lookup"><span data-stu-id="6362f-112">Example 1: Update an ANF volume</span></span>
```
PS C:\>Update-AzNetAppFilesVolume -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -Name "MyAnfVolume" -UsageThreshold Size

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool/volumes/MyAnfVolume
Name              : MyAnfAccount/MyAnfPool/MyAnfVolume
Type              : Microsoft.NetApp/netAppAccounts/capacityPools/volumes
Tags              :
FileSystemId      : 3e2773a7-2a72-d003-0637-1a8b1fa3eaaf
CreationToken     : MyAnfVolume
ServiceLevel      : Premium
UsageThreshold    : 2199023255552
ProvisioningState : Succeeded
SubnetId          : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.Network/virtualNetworks/MyRG-vnet/subnets/default
```

<span data-ttu-id="6362f-113">Эта команда обновляет ANF Volume "MyAnfVolume" с новым размером UsageThreshold.</span><span class="sxs-lookup"><span data-stu-id="6362f-113">This command updates the ANF volume "MyAnfVolume" with the new UsageThreshold size.</span></span>

## <span data-ttu-id="6362f-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6362f-114">PARAMETERS</span></span>

### <span data-ttu-id="6362f-115">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="6362f-115">-AccountName</span></span>
<span data-ttu-id="6362f-116">Имя учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="6362f-116">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6362f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6362f-117">-DefaultProfile</span></span>
<span data-ttu-id="6362f-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6362f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6362f-119">-ExportPolicy</span><span class="sxs-lookup"><span data-stu-id="6362f-119">-ExportPolicy</span></span>
<span data-ttu-id="6362f-120">Массив хэш-таблиц, который представляет политику экспорта</span><span class="sxs-lookup"><span data-stu-id="6362f-120">A hashtable array which represents the export policy</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolumeExportPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6362f-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6362f-121">-InputObject</span></span>
<span data-ttu-id="6362f-122">Объект тома для обновления</span><span class="sxs-lookup"><span data-stu-id="6362f-122">The volume object to update</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6362f-123">-Location</span><span class="sxs-lookup"><span data-stu-id="6362f-123">-Location</span></span>
<span data-ttu-id="6362f-124">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="6362f-124">The location of the resource</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6362f-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6362f-125">-Name</span></span>
<span data-ttu-id="6362f-126">Имя ANFого тома.</span><span class="sxs-lookup"><span data-stu-id="6362f-126">The name of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6362f-127">-PoolName</span><span class="sxs-lookup"><span data-stu-id="6362f-127">-PoolName</span></span>
<span data-ttu-id="6362f-128">Название пула ANF</span><span class="sxs-lookup"><span data-stu-id="6362f-128">The name of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6362f-129">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="6362f-129">-PoolObject</span></span>
<span data-ttu-id="6362f-130">Объект пула, содержащий том, который нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="6362f-130">The pool object containing the volume to update</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6362f-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6362f-131">-ResourceGroupName</span></span>
<span data-ttu-id="6362f-132">Группа ресурсов для учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="6362f-132">The resource group of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6362f-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6362f-133">-ResourceId</span></span>
<span data-ttu-id="6362f-134">Идентификатор ресурса ANFого тома.</span><span class="sxs-lookup"><span data-stu-id="6362f-134">The resource id of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6362f-135">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="6362f-135">-ServiceLevel</span></span>
<span data-ttu-id="6362f-136">Уровень обслуживания тома ANF</span><span class="sxs-lookup"><span data-stu-id="6362f-136">The service level of the ANF volume</span></span>

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

### <span data-ttu-id="6362f-137">-Тег</span><span class="sxs-lookup"><span data-stu-id="6362f-137">-Tag</span></span>
<span data-ttu-id="6362f-138">Хэш-таблица, представляющая Теги ресурсов</span><span class="sxs-lookup"><span data-stu-id="6362f-138">A hashtable which represents resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6362f-139">-UsageThreshold</span><span class="sxs-lookup"><span data-stu-id="6362f-139">-UsageThreshold</span></span>
<span data-ttu-id="6362f-140">Максимальная квота хранилища, разрешенная для файловой системы в байтах.</span><span class="sxs-lookup"><span data-stu-id="6362f-140">The maximum storage quota allowed for a file system in bytes</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6362f-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6362f-141">-Confirm</span></span>
<span data-ttu-id="6362f-142">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6362f-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6362f-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6362f-143">-WhatIf</span></span>
<span data-ttu-id="6362f-144">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6362f-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6362f-145">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6362f-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6362f-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6362f-146">CommonParameters</span></span>
<span data-ttu-id="6362f-147">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6362f-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6362f-148">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6362f-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6362f-149">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6362f-149">INPUTS</span></span>

### <span data-ttu-id="6362f-150">System. String</span><span class="sxs-lookup"><span data-stu-id="6362f-150">System.String</span></span>

### <span data-ttu-id="6362f-151">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="6362f-151">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="6362f-152">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="6362f-152">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="6362f-153">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6362f-153">OUTPUTS</span></span>

### <span data-ttu-id="6362f-154">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="6362f-154">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="6362f-155">Пуск</span><span class="sxs-lookup"><span data-stu-id="6362f-155">NOTES</span></span>

## <span data-ttu-id="6362f-156">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6362f-156">RELATED LINKS</span></span>
