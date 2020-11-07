---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesVolume.md
ms.openlocfilehash: b742c8af0e8c36d07b2c608e74f0a02349502104
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730770"
---
# <span data-ttu-id="35ada-101">New-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="35ada-101">New-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="35ada-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="35ada-102">SYNOPSIS</span></span>
<span data-ttu-id="35ada-103">Создание нового тома для файлов Azure NetApp (ANF).</span><span class="sxs-lookup"><span data-stu-id="35ada-103">Creates a new Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="35ada-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="35ada-104">SYNTAX</span></span>

### <span data-ttu-id="35ada-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="35ada-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesVolume -ResourceGroupName <String> -Location <String> -AccountName <String> -PoolName <String>
 -Name <String> -UsageThreshold <Int64> -SubnetId <String> -CreationToken <String> -ServiceLevel <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35ada-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="35ada-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesVolume -Name <String> -UsageThreshold <Int64> -SubnetId <String> -CreationToken <String>
 -ServiceLevel <String> [-Tag <Hashtable>] -PoolObject <PSNetAppFilesPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35ada-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="35ada-107">DESCRIPTION</span></span>
<span data-ttu-id="35ada-108">Командлет **New-AzNetAppFilesVolume** создает том ANF.</span><span class="sxs-lookup"><span data-stu-id="35ada-108">The **New-AzNetAppFilesVolume** cmdlet creates an ANF volume.</span></span>

## <span data-ttu-id="35ada-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="35ada-109">EXAMPLES</span></span>

### <span data-ttu-id="35ada-110">Пример 1: создание тома ANF</span><span class="sxs-lookup"><span data-stu-id="35ada-110">Example 1: Create an ANF volume</span></span>
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

<span data-ttu-id="35ada-111">Эта команда создает новый том ANF "MyAnfVolume" в пуле "MyAnfPool".</span><span class="sxs-lookup"><span data-stu-id="35ada-111">This command creates the new ANF volume "MyAnfVolume" within the pool "MyAnfPool".</span></span>

## <span data-ttu-id="35ada-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="35ada-112">PARAMETERS</span></span>

### <span data-ttu-id="35ada-113">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="35ada-113">-AccountName</span></span>
<span data-ttu-id="35ada-114">Имя учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="35ada-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="35ada-115">-CreationToken</span><span class="sxs-lookup"><span data-stu-id="35ada-115">-CreationToken</span></span>
<span data-ttu-id="35ada-116">Уникальный путь к файлу для тома</span><span class="sxs-lookup"><span data-stu-id="35ada-116">A unique file path for the volume</span></span>

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

### <span data-ttu-id="35ada-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35ada-117">-DefaultProfile</span></span>
<span data-ttu-id="35ada-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="35ada-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35ada-119">-Location</span><span class="sxs-lookup"><span data-stu-id="35ada-119">-Location</span></span>
<span data-ttu-id="35ada-120">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="35ada-120">The location of the resource</span></span>

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

### <span data-ttu-id="35ada-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="35ada-121">-Name</span></span>
<span data-ttu-id="35ada-122">Имя ANFого тома.</span><span class="sxs-lookup"><span data-stu-id="35ada-122">The name of the ANF volume</span></span>

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

### <span data-ttu-id="35ada-123">-PoolName</span><span class="sxs-lookup"><span data-stu-id="35ada-123">-PoolName</span></span>
<span data-ttu-id="35ada-124">Название пула ANF</span><span class="sxs-lookup"><span data-stu-id="35ada-124">The name of the ANF pool</span></span>

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

### <span data-ttu-id="35ada-125">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="35ada-125">-PoolObject</span></span>
<span data-ttu-id="35ada-126">Пул для нового объекта "Громкость"</span><span class="sxs-lookup"><span data-stu-id="35ada-126">The pool for the new volume object</span></span>

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

### <span data-ttu-id="35ada-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35ada-127">-ResourceGroupName</span></span>
<span data-ttu-id="35ada-128">Группа ресурсов для учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="35ada-128">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="35ada-129">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="35ada-129">-ServiceLevel</span></span>
<span data-ttu-id="35ada-130">Уровень обслуживания тома ANF</span><span class="sxs-lookup"><span data-stu-id="35ada-130">The service level of the ANF volume</span></span>

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

### <span data-ttu-id="35ada-131">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="35ada-131">-SubnetId</span></span>
<span data-ttu-id="35ada-132">Универсальный код ресурса (URI) Azure для подсети делегирования</span><span class="sxs-lookup"><span data-stu-id="35ada-132">The Azure Resource URI for a delegated subnet</span></span>

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

### <span data-ttu-id="35ada-133">-Тег</span><span class="sxs-lookup"><span data-stu-id="35ada-133">-Tag</span></span>
<span data-ttu-id="35ada-134">Хэш-таблица, представляющая Теги ресурсов</span><span class="sxs-lookup"><span data-stu-id="35ada-134">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="35ada-135">-UsageThreshold</span><span class="sxs-lookup"><span data-stu-id="35ada-135">-UsageThreshold</span></span>
<span data-ttu-id="35ada-136">Максимальная квота хранилища, разрешенная для файловой системы в байтах.</span><span class="sxs-lookup"><span data-stu-id="35ada-136">The maximum storage quota allowed for a file system in bytes</span></span>

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

### <span data-ttu-id="35ada-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="35ada-137">-Confirm</span></span>
<span data-ttu-id="35ada-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="35ada-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35ada-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35ada-139">-WhatIf</span></span>
<span data-ttu-id="35ada-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="35ada-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35ada-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="35ada-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35ada-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35ada-142">CommonParameters</span></span>
<span data-ttu-id="35ada-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="35ada-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="35ada-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35ada-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35ada-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="35ada-145">INPUTS</span></span>

### <span data-ttu-id="35ada-146">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="35ada-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="35ada-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="35ada-147">OUTPUTS</span></span>

### <span data-ttu-id="35ada-148">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="35ada-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="35ada-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="35ada-149">NOTES</span></span>

## <span data-ttu-id="35ada-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="35ada-150">RELATED LINKS</span></span>
