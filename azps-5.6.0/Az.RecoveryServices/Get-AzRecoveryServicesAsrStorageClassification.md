---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesasrstorageclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassification.md
ms.openlocfilehash: 441e3108053aa55c93ab0f9ee150bebd592a091e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985715"
---
# <span data-ttu-id="72e72-101">Get-AzRecoveryServicesAsrStorageClassification</span><span class="sxs-lookup"><span data-stu-id="72e72-101">Get-AzRecoveryServicesAsrStorageClassification</span></span>

## <span data-ttu-id="72e72-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72e72-102">SYNOPSIS</span></span>
<span data-ttu-id="72e72-103">Возвращает доступные (обнаруженные) классификации хранилища ASR в хранилище служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="72e72-103">Gets the available(discovered) ASR storage classifications in the Recovery Services vault.</span></span>

## <span data-ttu-id="72e72-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="72e72-104">SYNTAX</span></span>

### <span data-ttu-id="72e72-105">ByFabricObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="72e72-105">ByFabricObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrStorageClassification -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="72e72-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="72e72-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrStorageClassification -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72e72-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="72e72-107">ByObjectWithFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrStorageClassification -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72e72-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="72e72-108">DESCRIPTION</span></span>
<span data-ttu-id="72e72-109">**Cmdlet Get-AzRecoveryServicesAsrStorageClassification** получает подробные сведения об обнаруженных классификациях хранилища ASR в хранилище "Службы восстановления".</span><span class="sxs-lookup"><span data-stu-id="72e72-109">The **Get-AzRecoveryServicesAsrStorageClassification** cmdlet gets details of the discovered ASR storage classifications in the Recovery Services vault.</span></span>

## <span data-ttu-id="72e72-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="72e72-110">EXAMPLES</span></span>

### <span data-ttu-id="72e72-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="72e72-111">Example 1</span></span>
```
PS C:\> $StorageClassifications = Get-AzRecoveryServicesAsrStorageClassification -Fabric $Fabric
```

<span data-ttu-id="72e72-112">Укаймь обнаруженные классификации хранилища, соответствующие указанной тканью ASR.</span><span class="sxs-lookup"><span data-stu-id="72e72-112">List the discovered storage classifications corresponding to the specified ASR fabric.</span></span> 

## <span data-ttu-id="72e72-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="72e72-113">PARAMETERS</span></span>

### <span data-ttu-id="72e72-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72e72-114">-DefaultProfile</span></span>
<span data-ttu-id="72e72-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="72e72-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="72e72-116">-Ткань</span><span class="sxs-lookup"><span data-stu-id="72e72-116">-Fabric</span></span>
<span data-ttu-id="72e72-117">Определяет объект ткань asR.</span><span class="sxs-lookup"><span data-stu-id="72e72-117">Specifies an ASR fabric object.</span></span> <span data-ttu-id="72e72-118">Он получает сведения об обнаруженных классификациях хранилищ, соответствующих указанной структуре asR.</span><span class="sxs-lookup"><span data-stu-id="72e72-118">The cmdlet gets the details of discovered storage classifications corresponding to the specified ASR fabric.</span></span> 

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="72e72-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="72e72-119">-FriendlyName</span></span>
<span data-ttu-id="72e72-120">Указывает имя удобного объекта классификации хранилища, который нужно получить.</span><span class="sxs-lookup"><span data-stu-id="72e72-120">Specifies the friendly name of the storage classification object to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72e72-121">-Name</span><span class="sxs-lookup"><span data-stu-id="72e72-121">-Name</span></span>
<span data-ttu-id="72e72-122">Имя объекта классификации хранилища, который нужно получить.</span><span class="sxs-lookup"><span data-stu-id="72e72-122">Specifies the name of the storage classification object to get.</span></span>

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

### <span data-ttu-id="72e72-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72e72-123">CommonParameters</span></span>
<span data-ttu-id="72e72-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72e72-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72e72-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="72e72-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72e72-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="72e72-126">INPUTS</span></span>

### <span data-ttu-id="72e72-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span><span class="sxs-lookup"><span data-stu-id="72e72-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="72e72-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="72e72-128">OUTPUTS</span></span>

### <span data-ttu-id="72e72-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="72e72-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="72e72-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="72e72-130">NOTES</span></span>

## <span data-ttu-id="72e72-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="72e72-131">RELATED LINKS</span></span>
