---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesVolume.md
ms.openlocfilehash: 2214e84f4dd18981a8588ea32978a43e6d6e8045
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93911748"
---
# <span data-ttu-id="8a5f9-101">New-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="8a5f9-101">New-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="8a5f9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8a5f9-102">SYNOPSIS</span></span>
<span data-ttu-id="8a5f9-103">Создание нового тома для файлов Azure NetApp (ANF).</span><span class="sxs-lookup"><span data-stu-id="8a5f9-103">Creates a new Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="8a5f9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8a5f9-104">SYNTAX</span></span>

### <span data-ttu-id="8a5f9-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8a5f9-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesVolume -ResourceGroupName <String> -Location <String> -AccountName <String> -PoolName <String>
 -Name <String> -UsageThreshold <Int64> -SubnetId <String> -CreationToken <String> -ServiceLevel <String>
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>]
 [-ProtocolType <System.String[]>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a5f9-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8a5f9-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesVolume -Name <String> -UsageThreshold <Int64> -SubnetId <String> -CreationToken <String>
 -ServiceLevel <String> [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>]
 [-ProtocolType <System.String[]>]
 [-Tag <Hashtable>] -PoolObject <PSNetAppFilesPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a5f9-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8a5f9-107">DESCRIPTION</span></span>
<span data-ttu-id="8a5f9-108">Командлет **New-AzNetAppFilesVolume** создает том ANF.</span><span class="sxs-lookup"><span data-stu-id="8a5f9-108">The **New-AzNetAppFilesVolume** cmdlet creates an ANF volume.</span></span>

## <span data-ttu-id="8a5f9-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8a5f9-109">EXAMPLES</span></span>

### <span data-ttu-id="8a5f9-110">Пример 1: создание тома ANF</span><span class="sxs-lookup"><span data-stu-id="8a5f9-110">Example 1: Create an ANF volume</span></span>
```
PS C:\>New-AzNetAppFilesVolume -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -Name "MyAnfVolume" -l "westus2" -CreationToken "MyAnfVolume" -UsageThreshold 1099511627776 -ServiceLevel "Premium" -SubnetId "/subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.Network/virtualNetworks/MyVnetName/subnets/MySubNetName"

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool/volumes/MyAnfVolume
Name              : MyAnfAccount/MyAnfPool/MyAnfVolume
Type              : Microsoft.NetApp/netAppAccounts/capacityPools/volumes
Tags              :
FileSystemId      : 3e2773a7-2a72-d003-0637-1a8b1fa3eaaf
CreationToken     : MyAnfVolume
ServiceLevel      : Premium
UsageThreshold    : 1099511627776
ProvisioningState : Succeeded
SubnetId          : /subscriptions/f557b96d-2308-4a18-aae1-b8f7e7e70cc7/resourceGroups/MyRG/providers/Microsoft.Network/virtualNetworks/MyVnetName/subnets/default
```

<span data-ttu-id="8a5f9-111">Эта команда создает новый том ANF "MyAnfVolume" в пуле "MyAnfPool".</span><span class="sxs-lookup"><span data-stu-id="8a5f9-111">This command creates the new ANF volume "MyAnfVolume" within the pool "MyAnfPool".</span></span>

## <span data-ttu-id="8a5f9-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8a5f9-112">PARAMETERS</span></span>

### <span data-ttu-id="8a5f9-113">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="8a5f9-113">-AccountName</span></span>
<span data-ttu-id="8a5f9-114">Имя учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="8a5f9-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="8a5f9-115">-CreationToken</span><span class="sxs-lookup"><span data-stu-id="8a5f9-115">-CreationToken</span></span>
<span data-ttu-id="8a5f9-116">Уникальный путь к файлу для тома</span><span class="sxs-lookup"><span data-stu-id="8a5f9-116">A unique file path for the volume</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a5f9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a5f9-117">-DefaultProfile</span></span>
<span data-ttu-id="8a5f9-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8a5f9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a5f9-119">-ExportPolicy</span><span class="sxs-lookup"><span data-stu-id="8a5f9-119">-ExportPolicy</span></span>
<span data-ttu-id="8a5f9-120">Массив хэш-таблиц, который представляет политику экспорта</span><span class="sxs-lookup"><span data-stu-id="8a5f9-120">A hashtable array which represents the export policy</span></span>

```yaml
Type: PSNetAppFilesVolumeExportPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a5f9-121">-Location</span><span class="sxs-lookup"><span data-stu-id="8a5f9-121">-Location</span></span>
<span data-ttu-id="8a5f9-122">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="8a5f9-122">The location of the resource</span></span>

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

### <span data-ttu-id="8a5f9-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8a5f9-123">-Name</span></span>
<span data-ttu-id="8a5f9-124">Имя ANFого тома.</span><span class="sxs-lookup"><span data-stu-id="8a5f9-124">The name of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a5f9-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="8a5f9-125">-PoolName</span></span>
<span data-ttu-id="8a5f9-126">Название пула ANF</span><span class="sxs-lookup"><span data-stu-id="8a5f9-126">The name of the ANF pool</span></span>

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

### <span data-ttu-id="8a5f9-127">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="8a5f9-127">-PoolObject</span></span>
<span data-ttu-id="8a5f9-128">Пул для нового объекта "Громкость"</span><span class="sxs-lookup"><span data-stu-id="8a5f9-128">The pool for the new volume object</span></span>

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

### <span data-ttu-id="8a5f9-129">-ProtocolType</span><span class="sxs-lookup"><span data-stu-id="8a5f9-129">-ProtocolType</span></span>
<span data-ttu-id="8a5f9-130">Массив хэш-таблиц, который представляет политику экспорта</span><span class="sxs-lookup"><span data-stu-id="8a5f9-130">A hashtable array which represents the export policy</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a5f9-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a5f9-131">-ResourceGroupName</span></span>
<span data-ttu-id="8a5f9-132">Группа ресурсов для учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="8a5f9-132">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="8a5f9-133">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="8a5f9-133">-ServiceLevel</span></span>
<span data-ttu-id="8a5f9-134">Уровень обслуживания тома ANF</span><span class="sxs-lookup"><span data-stu-id="8a5f9-134">The service level of the ANF volume</span></span>

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

```yaml
Type: String
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a5f9-135">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="8a5f9-135">-SubnetId</span></span>
<span data-ttu-id="8a5f9-136">Универсальный код ресурса (URI) Azure для подсети делегирования</span><span class="sxs-lookup"><span data-stu-id="8a5f9-136">The Azure Resource URI for a delegated subnet</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a5f9-137">-Тег</span><span class="sxs-lookup"><span data-stu-id="8a5f9-137">-Tag</span></span>
<span data-ttu-id="8a5f9-138">Хэш-таблица, представляющая Теги ресурсов</span><span class="sxs-lookup"><span data-stu-id="8a5f9-138">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="8a5f9-139">-UsageThreshold</span><span class="sxs-lookup"><span data-stu-id="8a5f9-139">-UsageThreshold</span></span>
<span data-ttu-id="8a5f9-140">Максимальная квота хранилища, разрешенная для файловой системы в байтах.</span><span class="sxs-lookup"><span data-stu-id="8a5f9-140">The maximum storage quota allowed for a file system in bytes</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a5f9-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8a5f9-141">-Confirm</span></span>
<span data-ttu-id="8a5f9-142">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8a5f9-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a5f9-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a5f9-143">-WhatIf</span></span>
<span data-ttu-id="8a5f9-144">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8a5f9-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a5f9-145">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8a5f9-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a5f9-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a5f9-146">CommonParameters</span></span>
<span data-ttu-id="8a5f9-147">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8a5f9-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="8a5f9-148">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a5f9-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a5f9-149">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8a5f9-149">INPUTS</span></span>

### <span data-ttu-id="8a5f9-150">System. String</span><span class="sxs-lookup"><span data-stu-id="8a5f9-150">System.String</span></span>

### <span data-ttu-id="8a5f9-151">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="8a5f9-151">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="8a5f9-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8a5f9-152">OUTPUTS</span></span>

### <span data-ttu-id="8a5f9-153">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="8a5f9-153">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="8a5f9-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="8a5f9-154">NOTES</span></span>

## <span data-ttu-id="8a5f9-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8a5f9-155">RELATED LINKS</span></span>
