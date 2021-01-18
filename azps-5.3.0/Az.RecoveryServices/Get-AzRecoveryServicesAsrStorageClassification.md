---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrstorageclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassification.md
ms.openlocfilehash: a5265f6c824160ccd06022d54613818131f4da94
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98508101"
---
# <span data-ttu-id="a2c7f-101">Get-AzRecoveryServicesAsrStorageClassification</span><span class="sxs-lookup"><span data-stu-id="a2c7f-101">Get-AzRecoveryServicesAsrStorageClassification</span></span>

## <span data-ttu-id="a2c7f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2c7f-102">SYNOPSIS</span></span>
<span data-ttu-id="a2c7f-103">Возвращает доступные (обнаруженные) классификации хранилища ASR в хранилище служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="a2c7f-103">Gets the available(discovered) ASR storage classifications in the Recovery Services vault.</span></span>

## <span data-ttu-id="a2c7f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a2c7f-104">SYNTAX</span></span>

### <span data-ttu-id="a2c7f-105">ByFabricObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a2c7f-105">ByFabricObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrStorageClassification -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a2c7f-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="a2c7f-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrStorageClassification -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2c7f-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="a2c7f-107">ByObjectWithFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrStorageClassification -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a2c7f-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a2c7f-108">DESCRIPTION</span></span>
<span data-ttu-id="a2c7f-109">**Cmdlet Get-AzRecoveryServicesAsrStorageClassification** получает подробные сведения об обнаруженных классификациях хранилища ASR в хранилище "Службы восстановления".</span><span class="sxs-lookup"><span data-stu-id="a2c7f-109">The **Get-AzRecoveryServicesAsrStorageClassification** cmdlet gets details of the discovered ASR storage classifications in the Recovery Services vault.</span></span>

## <span data-ttu-id="a2c7f-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a2c7f-110">EXAMPLES</span></span>

### <span data-ttu-id="a2c7f-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a2c7f-111">Example 1</span></span>
```
PS C:\> $StorageClassifications = Get-AzRecoveryServicesAsrStorageClassification -Fabric $Fabric
```

<span data-ttu-id="a2c7f-112">Укаймь обнаруженные классификации хранилища, соответствующие указанной тканью ASR.</span><span class="sxs-lookup"><span data-stu-id="a2c7f-112">List the discovered storage classifications corresponding to the specified ASR fabric.</span></span> 

## <span data-ttu-id="a2c7f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a2c7f-113">PARAMETERS</span></span>

### <span data-ttu-id="a2c7f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2c7f-114">-DefaultProfile</span></span>
<span data-ttu-id="a2c7f-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a2c7f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="a2c7f-116">-Ткань</span><span class="sxs-lookup"><span data-stu-id="a2c7f-116">-Fabric</span></span>
<span data-ttu-id="a2c7f-117">Определяет объект тканью ASR.</span><span class="sxs-lookup"><span data-stu-id="a2c7f-117">Specifies an ASR fabric object.</span></span> <span data-ttu-id="a2c7f-118">Он получает сведения об обнаруженных классификациях хранилищ, соответствующих указанной структуре asR.</span><span class="sxs-lookup"><span data-stu-id="a2c7f-118">The cmdlet gets the details of discovered storage classifications corresponding to the specified ASR fabric.</span></span> 

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

### <span data-ttu-id="a2c7f-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="a2c7f-119">-FriendlyName</span></span>
<span data-ttu-id="a2c7f-120">Указывает имя удобного объекта классификации хранилища, который нужно получить.</span><span class="sxs-lookup"><span data-stu-id="a2c7f-120">Specifies the friendly name of the storage classification object to get.</span></span>

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

### <span data-ttu-id="a2c7f-121">-Name</span><span class="sxs-lookup"><span data-stu-id="a2c7f-121">-Name</span></span>
<span data-ttu-id="a2c7f-122">Имя объекта классификации хранилища, который нужно получить.</span><span class="sxs-lookup"><span data-stu-id="a2c7f-122">Specifies the name of the storage classification object to get.</span></span>

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

### <span data-ttu-id="a2c7f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2c7f-123">CommonParameters</span></span>
<span data-ttu-id="a2c7f-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2c7f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2c7f-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a2c7f-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2c7f-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a2c7f-126">INPUTS</span></span>

### <span data-ttu-id="a2c7f-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span><span class="sxs-lookup"><span data-stu-id="a2c7f-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="a2c7f-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a2c7f-128">OUTPUTS</span></span>

### <span data-ttu-id="a2c7f-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="a2c7f-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="a2c7f-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a2c7f-130">NOTES</span></span>

## <span data-ttu-id="a2c7f-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a2c7f-131">RELATED LINKS</span></span>
