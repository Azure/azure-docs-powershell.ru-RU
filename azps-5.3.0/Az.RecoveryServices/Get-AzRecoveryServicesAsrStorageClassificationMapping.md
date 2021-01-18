---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: e38a7b30622b8bb5dcbcf6912db7212465026687
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506020"
---
# <span data-ttu-id="b3282-101">Get-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="b3282-101">Get-AzRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="b3282-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3282-102">SYNOPSIS</span></span>
<span data-ttu-id="b3282-103">Возвращает сопоставления классификации хранилища ASR.</span><span class="sxs-lookup"><span data-stu-id="b3282-103">Gets ASR storage classification mappings.</span></span>

## <span data-ttu-id="b3282-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b3282-104">SYNTAX</span></span>

### <span data-ttu-id="b3282-105">ByObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b3282-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrStorageClassificationMapping -StorageClassification <ASRStorageClassification>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3282-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="b3282-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrStorageClassificationMapping -Name <String>
 -StorageClassification <ASRStorageClassification> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b3282-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b3282-107">DESCRIPTION</span></span>
<span data-ttu-id="b3282-108">Подробные сведения о сопоставлении классификации хранилища ASR получает cmdlet **Get-AzRecoveryServicesAsrStorageClassificationMapping.**</span><span class="sxs-lookup"><span data-stu-id="b3282-108">The **Get-AzRecoveryServicesAsrStorageClassificationMapping** cmdlet gets the details of an ASR storage classification mapping.</span></span>

## <span data-ttu-id="b3282-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b3282-109">EXAMPLES</span></span>

### <span data-ttu-id="b3282-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b3282-110">Example 1</span></span>
```
PS C:\> $StorageClassificationMappings = Get-AzRecoveryServicesAsrStorageClassificationMapping -StorageClassification $StorageClassification
```

<span data-ttu-id="b3282-111">Со списком всех сопоставлений классификации хранилища, соответствующих указанной классификации хранилища.</span><span class="sxs-lookup"><span data-stu-id="b3282-111">List all storage classification mappings corresponding to the specified storage classification.</span></span>

## <span data-ttu-id="b3282-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b3282-112">PARAMETERS</span></span>

### <span data-ttu-id="b3282-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3282-113">-DefaultProfile</span></span>
<span data-ttu-id="b3282-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b3282-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="b3282-115">-Name</span><span class="sxs-lookup"><span data-stu-id="b3282-115">-Name</span></span>
<span data-ttu-id="b3282-116">Указывает имя сопоставления классификации хранилища, которое нужно получить.</span><span class="sxs-lookup"><span data-stu-id="b3282-116">Specifies the name of the storage classification mapping to get.</span></span>

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

### <span data-ttu-id="b3282-117">-StorageClassification</span><span class="sxs-lookup"><span data-stu-id="b3282-117">-StorageClassification</span></span>
<span data-ttu-id="b3282-118">Объект классификации хранилища ASR.</span><span class="sxs-lookup"><span data-stu-id="b3282-118">Specifies an ASR storage classification object.</span></span> <span data-ttu-id="b3282-119">Этот cmdlet получает сопоставления классификации хранилища ASR, соответствующие указанной классификации хранилища.</span><span class="sxs-lookup"><span data-stu-id="b3282-119">The cmdlet gets ASR storage classification mappings corresponding to the specified storage classification</span></span> 

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

### <span data-ttu-id="b3282-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3282-120">CommonParameters</span></span>
<span data-ttu-id="b3282-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3282-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3282-122">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b3282-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3282-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b3282-123">INPUTS</span></span>

### <span data-ttu-id="b3282-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="b3282-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="b3282-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b3282-125">OUTPUTS</span></span>

### <span data-ttu-id="b3282-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="b3282-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span></span>

## <span data-ttu-id="b3282-127">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b3282-127">NOTES</span></span>

## <span data-ttu-id="b3282-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b3282-128">RELATED LINKS</span></span>

[<span data-ttu-id="b3282-129">New-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="b3282-129">New-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./New-AzRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="b3282-130">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="b3282-130">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Remove-AzRecoveryServicesAsrStorageClassificationMapping.md)
