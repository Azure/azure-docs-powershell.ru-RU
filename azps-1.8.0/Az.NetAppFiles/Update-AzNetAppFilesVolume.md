---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesVolume.md
ms.openlocfilehash: ea943c490a87dd4c62752b97753971f0941ed3b9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730758"
---
# <span data-ttu-id="49f25-101">Update-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="49f25-101">Update-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="49f25-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="49f25-102">SYNOPSIS</span></span>
<span data-ttu-id="49f25-103">Обновляет том Azure NetApp Files (ANF) в соответствии с необязательными модификаторами.</span><span class="sxs-lookup"><span data-stu-id="49f25-103">Updates an Azure NetApp Files (ANF) volume according to the optional modifiers provided.</span></span>

## <span data-ttu-id="49f25-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="49f25-104">SYNTAX</span></span>

### <span data-ttu-id="49f25-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="49f25-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesVolume -ResourceGroupName <String> -Location <String> -AccountName <String>
 -PoolName <String> -Name <String> [-UsageThreshold <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49f25-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="49f25-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesVolume -Name <String> [-UsageThreshold <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>]
 -PoolObject <PSNetAppFilesPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="49f25-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="49f25-107">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesVolume [-UsageThreshold <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>]
 -InputObject <PSNetAppFilesVolume> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="49f25-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="49f25-108">DESCRIPTION</span></span>
<span data-ttu-id="49f25-109">Командлет **Update-AzNetAppFilesVolume** ОБНОВЛЯЕТ том ANF.</span><span class="sxs-lookup"><span data-stu-id="49f25-109">The **Update-AzNetAppFilesVolume** cmdlet updates an ANF volume.</span></span>

## <span data-ttu-id="49f25-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="49f25-110">EXAMPLES</span></span>

### <span data-ttu-id="49f25-111">Пример 1: обновление тома ANF</span><span class="sxs-lookup"><span data-stu-id="49f25-111">Example 1: Update an ANF volume</span></span>
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

<span data-ttu-id="49f25-112">Эта команда обновляет ANF Volume "MyAnfVolume" с новым размером UsageThreshold.</span><span class="sxs-lookup"><span data-stu-id="49f25-112">This command updates the ANF volume "MyAnfVolume" with the new UsageThreshold size.</span></span>

## <span data-ttu-id="49f25-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="49f25-113">PARAMETERS</span></span>

### <span data-ttu-id="49f25-114">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="49f25-114">-AccountName</span></span>
<span data-ttu-id="49f25-115">Имя учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="49f25-115">The name of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49f25-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49f25-116">-DefaultProfile</span></span>
<span data-ttu-id="49f25-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="49f25-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49f25-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="49f25-118">-InputObject</span></span>
<span data-ttu-id="49f25-119">Объект тома для обновления</span><span class="sxs-lookup"><span data-stu-id="49f25-119">The volume object to update</span></span>

```yaml
Type: PSNetAppFilesVolume
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="49f25-120">-Location</span><span class="sxs-lookup"><span data-stu-id="49f25-120">-Location</span></span>
<span data-ttu-id="49f25-121">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="49f25-121">The location of the resource</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49f25-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="49f25-122">-Name</span></span>
<span data-ttu-id="49f25-123">Имя ANFого тома.</span><span class="sxs-lookup"><span data-stu-id="49f25-123">The name of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49f25-124">-PoolName</span><span class="sxs-lookup"><span data-stu-id="49f25-124">-PoolName</span></span>
<span data-ttu-id="49f25-125">Название пула ANF</span><span class="sxs-lookup"><span data-stu-id="49f25-125">The name of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49f25-126">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="49f25-126">-PoolObject</span></span>
<span data-ttu-id="49f25-127">Объект пула, содержащий том, который нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="49f25-127">The pool object containing the volume to update</span></span>

```yaml
Type: PSNetAppFilesPool
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="49f25-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49f25-128">-ResourceGroupName</span></span>
<span data-ttu-id="49f25-129">Группа ресурсов для учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="49f25-129">The resource group of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49f25-130">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="49f25-130">-ServiceLevel</span></span>
<span data-ttu-id="49f25-131">Уровень обслуживания тома ANF</span><span class="sxs-lookup"><span data-stu-id="49f25-131">The service level of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49f25-132">-Тег</span><span class="sxs-lookup"><span data-stu-id="49f25-132">-Tag</span></span>
<span data-ttu-id="49f25-133">Хэш-таблица, представляющая Теги ресурсов</span><span class="sxs-lookup"><span data-stu-id="49f25-133">A hashtable which represents resource tags</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49f25-134">-UsageThreshold</span><span class="sxs-lookup"><span data-stu-id="49f25-134">-UsageThreshold</span></span>
<span data-ttu-id="49f25-135">Максимальная квота хранилища, разрешенная для файловой системы в байтах.</span><span class="sxs-lookup"><span data-stu-id="49f25-135">The maximum storage quota allowed for a file system in bytes</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49f25-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="49f25-136">-Confirm</span></span>
<span data-ttu-id="49f25-137">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="49f25-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49f25-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49f25-138">-WhatIf</span></span>
<span data-ttu-id="49f25-139">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="49f25-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49f25-140">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="49f25-140">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49f25-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49f25-141">CommonParameters</span></span>
<span data-ttu-id="49f25-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="49f25-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="49f25-143">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49f25-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49f25-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="49f25-144">INPUTS</span></span>

### <span data-ttu-id="49f25-145">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="49f25-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="49f25-146">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="49f25-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="49f25-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="49f25-147">OUTPUTS</span></span>

### <span data-ttu-id="49f25-148">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="49f25-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="49f25-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="49f25-149">NOTES</span></span>

## <span data-ttu-id="49f25-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="49f25-150">RELATED LINKS</span></span>
