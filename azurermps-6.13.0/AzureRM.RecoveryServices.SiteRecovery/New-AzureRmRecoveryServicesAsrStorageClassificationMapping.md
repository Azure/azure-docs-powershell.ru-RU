---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: 6ab8102de0deb27c18c6e50f8d78db2f23a5155a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732459"
---
# <span data-ttu-id="d6ec5-101">New-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="d6ec5-101">New-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="d6ec5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d6ec5-102">SYNOPSIS</span></span>
<span data-ttu-id="d6ec5-103">Создание сопоставления классификации хранилища ASR в хранилище служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="d6ec5-103">Creates an ASR storage classification mapping in the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d6ec5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d6ec5-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesAsrStorageClassificationMapping -Name <String>
 -PrimaryStorageClassification <ASRStorageClassification>
 -RecoveryStorageClassification <ASRStorageClassification> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6ec5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d6ec5-105">DESCRIPTION</span></span>
<span data-ttu-id="d6ec5-106">Командлет **New-AzureRmRecoveryServicesAsrStorageClassificationMapping** создает классификацию хранилища для сопоставления хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="d6ec5-106">The **New-AzureRmRecoveryServicesAsrStorageClassificationMapping** cmdlet creates a storage classification mapping the Recovery Services vault.</span></span>

## <span data-ttu-id="d6ec5-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d6ec5-107">EXAMPLES</span></span>

### <span data-ttu-id="d6ec5-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d6ec5-108">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrStorageClassificationMapping -Name $StrorageClassificationMappingName -PrimaryStorageClassification $PrimaryStorageClassification -RecoveryStorageClassification $RecoveryStorageClassification
```

<span data-ttu-id="d6ec5-109">Запускает операцию создания сопоставления классификации хранилища с указанными параметрами и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="d6ec5-109">Starts the storage classification mapping creation operation with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="d6ec5-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d6ec5-110">PARAMETERS</span></span>

### <span data-ttu-id="d6ec5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6ec5-111">-DefaultProfile</span></span>
<span data-ttu-id="d6ec5-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d6ec5-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6ec5-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d6ec5-113">-Name</span></span>
<span data-ttu-id="d6ec5-114">Задает имя для сопоставления классификаций хранилища ASR.</span><span class="sxs-lookup"><span data-stu-id="d6ec5-114">Specifies a name for the ASR storage classification mapping.</span></span>

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

### <span data-ttu-id="d6ec5-115">-PrimaryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="d6ec5-115">-PrimaryStorageClassification</span></span>
<span data-ttu-id="d6ec5-116">Задает основной объект классификации хранилища ASR для сопоставления.</span><span class="sxs-lookup"><span data-stu-id="d6ec5-116">Specifies the primary ASR storage classification object for the mapping.</span></span>

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

### <span data-ttu-id="d6ec5-117">-RecoveryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="d6ec5-117">-RecoveryStorageClassification</span></span>
<span data-ttu-id="d6ec5-118">Указывает объект классификации хранилища для восстановления ASR для сопоставления.</span><span class="sxs-lookup"><span data-stu-id="d6ec5-118">Specifies the recovery ASR storage classification object for the mapping.</span></span>

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

### <span data-ttu-id="d6ec5-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d6ec5-119">-Confirm</span></span>
<span data-ttu-id="d6ec5-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d6ec5-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6ec5-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6ec5-121">-WhatIf</span></span>
<span data-ttu-id="d6ec5-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d6ec5-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d6ec5-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d6ec5-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6ec5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6ec5-124">CommonParameters</span></span>
<span data-ttu-id="d6ec5-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d6ec5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6ec5-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6ec5-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6ec5-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d6ec5-127">INPUTS</span></span>

### <span data-ttu-id="d6ec5-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="d6ec5-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="d6ec5-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d6ec5-129">OUTPUTS</span></span>

### <span data-ttu-id="d6ec5-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="d6ec5-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="d6ec5-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="d6ec5-131">NOTES</span></span>

## <span data-ttu-id="d6ec5-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d6ec5-132">RELATED LINKS</span></span>

[<span data-ttu-id="d6ec5-133">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="d6ec5-133">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./Get-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="d6ec5-134">Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="d6ec5-134">Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)
