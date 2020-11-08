---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: 091f8892238d88554d0e0c3502ffbeb8e8d4c154
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94072687"
---
# <span data-ttu-id="2f830-101">New-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="2f830-101">New-AzRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="2f830-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2f830-102">SYNOPSIS</span></span>
<span data-ttu-id="2f830-103">Создание сопоставления классификации хранилища ASR в хранилище служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="2f830-103">Creates an ASR storage classification mapping in the Recovery Services vault.</span></span>

## <span data-ttu-id="2f830-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2f830-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrStorageClassificationMapping -Name <String>
 -PrimaryStorageClassification <ASRStorageClassification>
 -RecoveryStorageClassification <ASRStorageClassification> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f830-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2f830-105">DESCRIPTION</span></span>
<span data-ttu-id="2f830-106">Командлет **New-AzRecoveryServicesAsrStorageClassificationMapping** создает классификацию хранилища для сопоставления хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="2f830-106">The **New-AzRecoveryServicesAsrStorageClassificationMapping** cmdlet creates a storage classification mapping the Recovery Services vault.</span></span>

## <span data-ttu-id="2f830-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2f830-107">EXAMPLES</span></span>

### <span data-ttu-id="2f830-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2f830-108">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrStorageClassificationMapping -Name $StorageClassificationMappingName -PrimaryStorageClassification $PrimaryStorageClassification -RecoveryStorageClassification $RecoveryStorageClassification
```

<span data-ttu-id="2f830-109">Запускает операцию создания сопоставления классификации хранилища с указанными параметрами и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="2f830-109">Starts the storage classification mapping creation operation with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="2f830-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2f830-110">PARAMETERS</span></span>

### <span data-ttu-id="2f830-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f830-111">-DefaultProfile</span></span>
<span data-ttu-id="2f830-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2f830-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="2f830-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2f830-113">-Name</span></span>
<span data-ttu-id="2f830-114">Задает имя для сопоставления классификаций хранилища ASR.</span><span class="sxs-lookup"><span data-stu-id="2f830-114">Specifies a name for the ASR storage classification mapping.</span></span>

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

### <span data-ttu-id="2f830-115">-PrimaryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="2f830-115">-PrimaryStorageClassification</span></span>
<span data-ttu-id="2f830-116">Задает основной объект классификации хранилища ASR для сопоставления.</span><span class="sxs-lookup"><span data-stu-id="2f830-116">Specifies the primary ASR storage classification object for the mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2f830-117">-RecoveryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="2f830-117">-RecoveryStorageClassification</span></span>
<span data-ttu-id="2f830-118">Указывает объект классификации хранилища для восстановления ASR для сопоставления.</span><span class="sxs-lookup"><span data-stu-id="2f830-118">Specifies the recovery ASR storage classification object for the mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f830-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2f830-119">-Confirm</span></span>
<span data-ttu-id="2f830-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2f830-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f830-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f830-121">-WhatIf</span></span>
<span data-ttu-id="2f830-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2f830-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2f830-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2f830-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f830-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f830-124">CommonParameters</span></span>
<span data-ttu-id="2f830-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2f830-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f830-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2f830-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f830-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2f830-127">INPUTS</span></span>

### <span data-ttu-id="2f830-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="2f830-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="2f830-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2f830-129">OUTPUTS</span></span>

### <span data-ttu-id="2f830-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="2f830-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="2f830-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="2f830-131">NOTES</span></span>

## <span data-ttu-id="2f830-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2f830-132">RELATED LINKS</span></span>

[<span data-ttu-id="2f830-133">Get-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="2f830-133">Get-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Get-AzRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="2f830-134">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="2f830-134">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Remove-AzRecoveryServicesAsrStorageClassificationMapping.md)
