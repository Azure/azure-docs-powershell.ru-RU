---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrinmageazurev2diskinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrInMageAzureV2DiskInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrInMageAzureV2DiskInput.md
ms.openlocfilehash: 115287c5892a83cd38e20080cdaee8ff531a612d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94234795"
---
# <span data-ttu-id="a4c75-101">New-AzRecoveryServicesAsrInMageAzureV2DiskInput</span><span class="sxs-lookup"><span data-stu-id="a4c75-101">New-AzRecoveryServicesAsrInMageAzureV2DiskInput</span></span>

## <span data-ttu-id="a4c75-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a4c75-102">SYNOPSIS</span></span>
<span data-ttu-id="a4c75-103">Создает объект сопоставления дисков для реплицируемых дисков виртуальных машин vMWare.</span><span class="sxs-lookup"><span data-stu-id="a4c75-103">Creates a disk mapping object for vMWare virtual machine disks to be replicated.</span></span>

## <span data-ttu-id="a4c75-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a4c75-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId <String> -LogStorageAccountId <String>
 -DiskType <String> [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4c75-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a4c75-105">DESCRIPTION</span></span>
<span data-ttu-id="a4c75-106">Создает объект сопоставления диска, который сопоставляет диск виртуального компьютера vMWare с учетной записью хранения кэша и целевым типом диска (область восстановления), который будет использоваться для репликации диска.</span><span class="sxs-lookup"><span data-stu-id="a4c75-106">Creates a disk mapping object that maps an vMWare virtual machine disk to the cache storage account and target managed disk type (recovery region) to be used to replicate the disk.</span></span>

## <span data-ttu-id="a4c75-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a4c75-107">EXAMPLES</span></span>

### <span data-ttu-id="a4c75-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a4c75-108">Example 1</span></span>
```powershell
PS C:> New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId $diskId -LogStorageAccountId $logStorageAccountId -DiskType $diskType
```

<span data-ttu-id="a4c75-109">Создайте объект сопоставления дисков для дисков виртуальных машин vMWare, которые нужно реплицировать. Используется во время включения защиты для компьютера vMWare.</span><span class="sxs-lookup"><span data-stu-id="a4c75-109">Create a disk mapping object for vMWare virtual machine disks to be replicated.Used during enable protection for vMWare machine.</span></span>

## <span data-ttu-id="a4c75-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a4c75-110">PARAMETERS</span></span>

### <span data-ttu-id="a4c75-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4c75-111">-DefaultProfile</span></span>
<span data-ttu-id="a4c75-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a4c75-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4c75-113">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="a4c75-113">-DiskEncryptionSetId</span></span>
<span data-ttu-id="a4c75-114">Указывает идентификатор ресурса набора шифрования диска, который будет использоваться для шифрования управляемых дисков.</span><span class="sxs-lookup"><span data-stu-id="a4c75-114">Specifies the resource Id of the disk encryption set, to be used for the encryption of the managed disks.</span></span>

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

### <span data-ttu-id="a4c75-115">-DiskId</span><span class="sxs-lookup"><span data-stu-id="a4c75-115">-DiskId</span></span>
<span data-ttu-id="a4c75-116">Укажите DiskId диска, которому соответствует это сопоставление.</span><span class="sxs-lookup"><span data-stu-id="a4c75-116">Specify the DiskId of the disk that this mapping corresponds to.</span></span>

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

### <span data-ttu-id="a4c75-117">-DiskType</span><span class="sxs-lookup"><span data-stu-id="a4c75-117">-DiskType</span></span>
<span data-ttu-id="a4c75-118">Указывает тип диска для восстановления.</span><span class="sxs-lookup"><span data-stu-id="a4c75-118">Specifies the Recovery disk type.</span></span>

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

### <span data-ttu-id="a4c75-119">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="a4c75-119">-LogStorageAccountId</span></span>
<span data-ttu-id="a4c75-120">Указывает идентификатор журнала или учетной записи для хранения кэша, который будет использоваться для хранения журналов репликации.</span><span class="sxs-lookup"><span data-stu-id="a4c75-120">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

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

### <span data-ttu-id="a4c75-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a4c75-121">-Confirm</span></span>
<span data-ttu-id="a4c75-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a4c75-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4c75-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4c75-123">-WhatIf</span></span>
<span data-ttu-id="a4c75-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a4c75-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4c75-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a4c75-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4c75-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4c75-126">CommonParameters</span></span>
<span data-ttu-id="a4c75-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a4c75-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4c75-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a4c75-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4c75-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a4c75-129">INPUTS</span></span>

### <span data-ttu-id="a4c75-130">Ничего</span><span class="sxs-lookup"><span data-stu-id="a4c75-130">None</span></span>

## <span data-ttu-id="a4c75-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a4c75-131">OUTPUTS</span></span>

### <span data-ttu-id="a4c75-132">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. AsrInMageAzureV2DiskInput</span><span class="sxs-lookup"><span data-stu-id="a4c75-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.AsrInMageAzureV2DiskInput</span></span>

## <span data-ttu-id="a4c75-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="a4c75-133">NOTES</span></span>

## <span data-ttu-id="a4c75-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a4c75-134">RELATED LINKS</span></span>
