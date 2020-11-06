---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: 53a877543cc3811ccf52d240025135fefa3ede0b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563428"
---
# <span data-ttu-id="f39d2-101">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="f39d2-101">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="f39d2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f39d2-102">SYNOPSIS</span></span>
<span data-ttu-id="f39d2-103">Возвращает сопоставления классификаций хранилища ASR.</span><span class="sxs-lookup"><span data-stu-id="f39d2-103">Gets ASR storage classification mappings.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f39d2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f39d2-104">SYNTAX</span></span>

### <span data-ttu-id="f39d2-105">ByObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f39d2-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrStorageClassificationMapping -StorageClassification <ASRStorageClassification>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f39d2-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="f39d2-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrStorageClassificationMapping -Name <String>
 -StorageClassification <ASRStorageClassification> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f39d2-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f39d2-107">DESCRIPTION</span></span>
<span data-ttu-id="f39d2-108">Командлет **Get-AzureRmRecoveryServicesAsrStorageClassificationMapping** получает сведения о сопоставлении классификаций хранилища ASR.</span><span class="sxs-lookup"><span data-stu-id="f39d2-108">The **Get-AzureRmRecoveryServicesAsrStorageClassificationMapping** cmdlet gets the details of an ASR storage classification mapping.</span></span>

## <span data-ttu-id="f39d2-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f39d2-109">EXAMPLES</span></span>

### <span data-ttu-id="f39d2-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f39d2-110">Example 1</span></span>
```
PS C:\> $StorageClassificationMappings = Get-AzureRmRecoveryServicesAsrStorageClassificationMapping -StorageClassification $StorageClassification
```

<span data-ttu-id="f39d2-111">Перечислите все сопоставления классификаций хранилища, соответствующие указанной классификации хранилища.</span><span class="sxs-lookup"><span data-stu-id="f39d2-111">List all storage classification mappings corresponding to the specified storage classification.</span></span>

## <span data-ttu-id="f39d2-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f39d2-112">PARAMETERS</span></span>

### <span data-ttu-id="f39d2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f39d2-113">-DefaultProfile</span></span>
<span data-ttu-id="f39d2-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f39d2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f39d2-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f39d2-115">-Name</span></span>
<span data-ttu-id="f39d2-116">Указывает имя сопоставления классификации хранилища, которое требуется получить.</span><span class="sxs-lookup"><span data-stu-id="f39d2-116">Specifies the name of the storage classification mapping to get.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f39d2-117">-StorageClassification</span><span class="sxs-lookup"><span data-stu-id="f39d2-117">-StorageClassification</span></span>
<span data-ttu-id="f39d2-118">Указывает объект классификации хранилища ASR.</span><span class="sxs-lookup"><span data-stu-id="f39d2-118">Specifies an ASR storage classification object.</span></span> <span data-ttu-id="f39d2-119">Командлет возвращает сопоставления для классификации хранилища ASR, соответствующие указанной классификации хранилища.</span><span class="sxs-lookup"><span data-stu-id="f39d2-119">The cmdlet gets ASR storage classification mappings corresponding to the specified storage classification</span></span> 

```yaml
Type: ASRStorageClassification
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f39d2-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f39d2-120">CommonParameters</span></span>
<span data-ttu-id="f39d2-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f39d2-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f39d2-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f39d2-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f39d2-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f39d2-123">INPUTS</span></span>

### <span data-ttu-id="f39d2-124">Ничего</span><span class="sxs-lookup"><span data-stu-id="f39d2-124">None</span></span>

## <span data-ttu-id="f39d2-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f39d2-125">OUTPUTS</span></span>

### <span data-ttu-id="f39d2-126">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRStorageClassificationMapping, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="f39d2-126">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="f39d2-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="f39d2-127">NOTES</span></span>

## <span data-ttu-id="f39d2-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f39d2-128">RELATED LINKS</span></span>

[<span data-ttu-id="f39d2-129">New-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="f39d2-129">New-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./New-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="f39d2-130">Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="f39d2-130">Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)
