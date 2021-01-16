---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrinmageazurev2diskinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrInMageAzureV2DiskInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrInMageAzureV2DiskInput.md
ms.openlocfilehash: 115287c5892a83cd38e20080cdaee8ff531a612d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506799"
---
# <span data-ttu-id="0b305-101">New-AzRecoveryServicesAsrInMageAzureV2DiskInput</span><span class="sxs-lookup"><span data-stu-id="0b305-101">New-AzRecoveryServicesAsrInMageAzureV2DiskInput</span></span>

## <span data-ttu-id="0b305-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b305-102">SYNOPSIS</span></span>
<span data-ttu-id="0b305-103">Создает объект сопоставления дисков для реплицируемых дисков виртуальной машины vMWare.</span><span class="sxs-lookup"><span data-stu-id="0b305-103">Creates a disk mapping object for vMWare virtual machine disks to be replicated.</span></span>

## <span data-ttu-id="0b305-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0b305-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId <String> -LogStorageAccountId <String>
 -DiskType <String> [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b305-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0b305-105">DESCRIPTION</span></span>
<span data-ttu-id="0b305-106">Создание объекта сопоставления дисков, который сопоставлен с диском виртуальной машины vMWare с учетной записью хранения кэша и целевым управляемым типом диска (регионом восстановления), который будет использоваться для репликации диска.</span><span class="sxs-lookup"><span data-stu-id="0b305-106">Creates a disk mapping object that maps an vMWare virtual machine disk to the cache storage account and target managed disk type (recovery region) to be used to replicate the disk.</span></span>

## <span data-ttu-id="0b305-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0b305-107">EXAMPLES</span></span>

### <span data-ttu-id="0b305-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0b305-108">Example 1</span></span>
```powershell
PS C:> New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId $diskId -LogStorageAccountId $logStorageAccountId -DiskType $diskType
```

<span data-ttu-id="0b305-109">Создайте объект сопоставления дисков для дисковых дисков виртуальной машины vMWare, которые нужно реплицировать. Используется во время защиты компьютера vMWare.</span><span class="sxs-lookup"><span data-stu-id="0b305-109">Create a disk mapping object for vMWare virtual machine disks to be replicated.Used during enable protection for vMWare machine.</span></span>

## <span data-ttu-id="0b305-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0b305-110">PARAMETERS</span></span>

### <span data-ttu-id="0b305-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b305-111">-DefaultProfile</span></span>
<span data-ttu-id="0b305-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0b305-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b305-113">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="0b305-113">-DiskEncryptionSetId</span></span>
<span data-ttu-id="0b305-114">Определяет код ресурса набора шифрования диска, который будет использоваться для шифрования управляемых дисков.</span><span class="sxs-lookup"><span data-stu-id="0b305-114">Specifies the resource Id of the disk encryption set, to be used for the encryption of the managed disks.</span></span>

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

### <span data-ttu-id="0b305-115">-DiskId</span><span class="sxs-lookup"><span data-stu-id="0b305-115">-DiskId</span></span>
<span data-ttu-id="0b305-116">Укажите DiskId диска, на который это сопоставление указывается.</span><span class="sxs-lookup"><span data-stu-id="0b305-116">Specify the DiskId of the disk that this mapping corresponds to.</span></span>

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

### <span data-ttu-id="0b305-117">-DiskType</span><span class="sxs-lookup"><span data-stu-id="0b305-117">-DiskType</span></span>
<span data-ttu-id="0b305-118">Определяет тип диска восстановления.</span><span class="sxs-lookup"><span data-stu-id="0b305-118">Specifies the Recovery disk type.</span></span>

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

### <span data-ttu-id="0b305-119">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="0b305-119">-LogStorageAccountId</span></span>
<span data-ttu-id="0b305-120">Определяет ИД учетной записи хранения журнала или кэша, который будет использоваться для хранения журналов репликации.</span><span class="sxs-lookup"><span data-stu-id="0b305-120">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

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

### <span data-ttu-id="0b305-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0b305-121">-Confirm</span></span>
<span data-ttu-id="0b305-122">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="0b305-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b305-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b305-123">-WhatIf</span></span>
<span data-ttu-id="0b305-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0b305-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b305-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="0b305-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b305-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b305-126">CommonParameters</span></span>
<span data-ttu-id="0b305-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b305-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b305-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0b305-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b305-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0b305-129">INPUTS</span></span>

### <span data-ttu-id="0b305-130">Нет</span><span class="sxs-lookup"><span data-stu-id="0b305-130">None</span></span>

## <span data-ttu-id="0b305-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0b305-131">OUTPUTS</span></span>

### <span data-ttu-id="0b305-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.AsrInMageAzureV2DiskInput</span><span class="sxs-lookup"><span data-stu-id="0b305-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.AsrInMageAzureV2DiskInput</span></span>

## <span data-ttu-id="0b305-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0b305-133">NOTES</span></span>

## <span data-ttu-id="0b305-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0b305-134">RELATED LINKS</span></span>
