---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: e38a7b30622b8bb5dcbcf6912db7212465026687
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100227068"
---
# <span data-ttu-id="499b0-101">Get-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="499b0-101">Get-AzRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="499b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="499b0-102">SYNOPSIS</span></span>
<span data-ttu-id="499b0-103">Возвращает сопоставления классификации хранилища ASR.</span><span class="sxs-lookup"><span data-stu-id="499b0-103">Gets ASR storage classification mappings.</span></span>

## <span data-ttu-id="499b0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="499b0-104">SYNTAX</span></span>

### <span data-ttu-id="499b0-105">ByObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="499b0-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrStorageClassificationMapping -StorageClassification <ASRStorageClassification>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="499b0-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="499b0-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrStorageClassificationMapping -Name <String>
 -StorageClassification <ASRStorageClassification> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="499b0-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="499b0-107">DESCRIPTION</span></span>
<span data-ttu-id="499b0-108">Подробные сведения о сопоставлении классификации хранилища ASR получает cmdlet **Get-AzRecoveryServicesAsrStorageClassificationMapping.**</span><span class="sxs-lookup"><span data-stu-id="499b0-108">The **Get-AzRecoveryServicesAsrStorageClassificationMapping** cmdlet gets the details of an ASR storage classification mapping.</span></span>

## <span data-ttu-id="499b0-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="499b0-109">EXAMPLES</span></span>

### <span data-ttu-id="499b0-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="499b0-110">Example 1</span></span>
```
PS C:\> $StorageClassificationMappings = Get-AzRecoveryServicesAsrStorageClassificationMapping -StorageClassification $StorageClassification
```

<span data-ttu-id="499b0-111">Со списком всех сопоставлений классификации хранилища, соответствующих указанной классификации хранилища.</span><span class="sxs-lookup"><span data-stu-id="499b0-111">List all storage classification mappings corresponding to the specified storage classification.</span></span>

## <span data-ttu-id="499b0-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="499b0-112">PARAMETERS</span></span>

### <span data-ttu-id="499b0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="499b0-113">-DefaultProfile</span></span>
<span data-ttu-id="499b0-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="499b0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="499b0-115">-Name</span><span class="sxs-lookup"><span data-stu-id="499b0-115">-Name</span></span>
<span data-ttu-id="499b0-116">Указывает имя сопоставления классификации хранилища, которое нужно получить.</span><span class="sxs-lookup"><span data-stu-id="499b0-116">Specifies the name of the storage classification mapping to get.</span></span>

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

### <span data-ttu-id="499b0-117">-StorageClassification</span><span class="sxs-lookup"><span data-stu-id="499b0-117">-StorageClassification</span></span>
<span data-ttu-id="499b0-118">Объект классификации хранилища ASR.</span><span class="sxs-lookup"><span data-stu-id="499b0-118">Specifies an ASR storage classification object.</span></span> <span data-ttu-id="499b0-119">Этот cmdlet получает сопоставления классификации хранилища ASR, соответствующие указанной классификации хранилища.</span><span class="sxs-lookup"><span data-stu-id="499b0-119">The cmdlet gets ASR storage classification mappings corresponding to the specified storage classification</span></span> 

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

### <span data-ttu-id="499b0-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="499b0-120">CommonParameters</span></span>
<span data-ttu-id="499b0-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="499b0-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="499b0-122">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="499b0-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="499b0-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="499b0-123">INPUTS</span></span>

### <span data-ttu-id="499b0-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="499b0-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="499b0-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="499b0-125">OUTPUTS</span></span>

### <span data-ttu-id="499b0-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="499b0-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span></span>

## <span data-ttu-id="499b0-127">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="499b0-127">NOTES</span></span>

## <span data-ttu-id="499b0-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="499b0-128">RELATED LINKS</span></span>

[<span data-ttu-id="499b0-129">New-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="499b0-129">New-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./New-AzRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="499b0-130">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="499b0-130">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Remove-AzRecoveryServicesAsrStorageClassificationMapping.md)
