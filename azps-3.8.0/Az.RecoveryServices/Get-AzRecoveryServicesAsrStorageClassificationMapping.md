---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: e38a7b30622b8bb5dcbcf6912db7212465026687
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065075"
---
# <span data-ttu-id="f2501-101">Get-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="f2501-101">Get-AzRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="f2501-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f2501-102">SYNOPSIS</span></span>
<span data-ttu-id="f2501-103">Возвращает сопоставления классификаций хранилища ASR.</span><span class="sxs-lookup"><span data-stu-id="f2501-103">Gets ASR storage classification mappings.</span></span>

## <span data-ttu-id="f2501-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f2501-104">SYNTAX</span></span>

### <span data-ttu-id="f2501-105">ByObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f2501-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrStorageClassificationMapping -StorageClassification <ASRStorageClassification>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f2501-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="f2501-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrStorageClassificationMapping -Name <String>
 -StorageClassification <ASRStorageClassification> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f2501-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f2501-107">DESCRIPTION</span></span>
<span data-ttu-id="f2501-108">Командлет **Get-AzRecoveryServicesAsrStorageClassificationMapping** получает сведения о сопоставлении классификаций хранилища ASR.</span><span class="sxs-lookup"><span data-stu-id="f2501-108">The **Get-AzRecoveryServicesAsrStorageClassificationMapping** cmdlet gets the details of an ASR storage classification mapping.</span></span>

## <span data-ttu-id="f2501-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f2501-109">EXAMPLES</span></span>

### <span data-ttu-id="f2501-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f2501-110">Example 1</span></span>
```
PS C:\> $StorageClassificationMappings = Get-AzRecoveryServicesAsrStorageClassificationMapping -StorageClassification $StorageClassification
```

<span data-ttu-id="f2501-111">Перечислите все сопоставления классификаций хранилища, соответствующие указанной классификации хранилища.</span><span class="sxs-lookup"><span data-stu-id="f2501-111">List all storage classification mappings corresponding to the specified storage classification.</span></span>

## <span data-ttu-id="f2501-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f2501-112">PARAMETERS</span></span>

### <span data-ttu-id="f2501-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2501-113">-DefaultProfile</span></span>
<span data-ttu-id="f2501-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f2501-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="f2501-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f2501-115">-Name</span></span>
<span data-ttu-id="f2501-116">Указывает имя сопоставления классификации хранилища, которое требуется получить.</span><span class="sxs-lookup"><span data-stu-id="f2501-116">Specifies the name of the storage classification mapping to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2501-117">-StorageClassification</span><span class="sxs-lookup"><span data-stu-id="f2501-117">-StorageClassification</span></span>
<span data-ttu-id="f2501-118">Указывает объект классификации хранилища ASR.</span><span class="sxs-lookup"><span data-stu-id="f2501-118">Specifies an ASR storage classification object.</span></span> <span data-ttu-id="f2501-119">Командлет возвращает сопоставления для классификации хранилища ASR, соответствующие указанной классификации хранилища.</span><span class="sxs-lookup"><span data-stu-id="f2501-119">The cmdlet gets ASR storage classification mappings corresponding to the specified storage classification</span></span> 

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

### <span data-ttu-id="f2501-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2501-120">CommonParameters</span></span>
<span data-ttu-id="f2501-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f2501-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2501-122">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f2501-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2501-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f2501-123">INPUTS</span></span>

### <span data-ttu-id="f2501-124">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="f2501-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="f2501-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f2501-125">OUTPUTS</span></span>

### <span data-ttu-id="f2501-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="f2501-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span></span>

## <span data-ttu-id="f2501-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="f2501-127">NOTES</span></span>

## <span data-ttu-id="f2501-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f2501-128">RELATED LINKS</span></span>

[<span data-ttu-id="f2501-129">New-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="f2501-129">New-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./New-AzRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="f2501-130">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="f2501-130">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Remove-AzRecoveryServicesAsrStorageClassificationMapping.md)
