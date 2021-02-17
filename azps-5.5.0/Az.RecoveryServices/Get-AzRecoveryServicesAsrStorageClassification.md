---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrstorageclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassification.md
ms.openlocfilehash: a5265f6c824160ccd06022d54613818131f4da94
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100236100"
---
# <span data-ttu-id="2b092-101">Get-AzRecoveryServicesAsrStorageClassification</span><span class="sxs-lookup"><span data-stu-id="2b092-101">Get-AzRecoveryServicesAsrStorageClassification</span></span>

## <span data-ttu-id="2b092-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b092-102">SYNOPSIS</span></span>
<span data-ttu-id="2b092-103">Возвращает доступные (обнаруженные) классификации хранилища ASR в хранилище служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="2b092-103">Gets the available(discovered) ASR storage classifications in the Recovery Services vault.</span></span>

## <span data-ttu-id="2b092-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2b092-104">SYNTAX</span></span>

### <span data-ttu-id="2b092-105">ByFabricObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2b092-105">ByFabricObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrStorageClassification -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2b092-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="2b092-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrStorageClassification -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2b092-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="2b092-107">ByObjectWithFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrStorageClassification -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2b092-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2b092-108">DESCRIPTION</span></span>
<span data-ttu-id="2b092-109">**Cmdlet Get-AzRecoveryServicesAsrStorageClassification** получает подробные сведения об обнаруженных классификациях хранилища ASR в хранилище "Службы восстановления".</span><span class="sxs-lookup"><span data-stu-id="2b092-109">The **Get-AzRecoveryServicesAsrStorageClassification** cmdlet gets details of the discovered ASR storage classifications in the Recovery Services vault.</span></span>

## <span data-ttu-id="2b092-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2b092-110">EXAMPLES</span></span>

### <span data-ttu-id="2b092-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2b092-111">Example 1</span></span>
```
PS C:\> $StorageClassifications = Get-AzRecoveryServicesAsrStorageClassification -Fabric $Fabric
```

<span data-ttu-id="2b092-112">Укаймь обнаруженные классификации хранилища, соответствующие указанной тканью ASR.</span><span class="sxs-lookup"><span data-stu-id="2b092-112">List the discovered storage classifications corresponding to the specified ASR fabric.</span></span> 

## <span data-ttu-id="2b092-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2b092-113">PARAMETERS</span></span>

### <span data-ttu-id="2b092-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b092-114">-DefaultProfile</span></span>
<span data-ttu-id="2b092-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2b092-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="2b092-116">-Ткань</span><span class="sxs-lookup"><span data-stu-id="2b092-116">-Fabric</span></span>
<span data-ttu-id="2b092-117">Определяет объект тканью ASR.</span><span class="sxs-lookup"><span data-stu-id="2b092-117">Specifies an ASR fabric object.</span></span> <span data-ttu-id="2b092-118">Он получает сведения об обнаруженных классификациях хранилищ, соответствующих указанной структуре asR.</span><span class="sxs-lookup"><span data-stu-id="2b092-118">The cmdlet gets the details of discovered storage classifications corresponding to the specified ASR fabric.</span></span> 

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

### <span data-ttu-id="2b092-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="2b092-119">-FriendlyName</span></span>
<span data-ttu-id="2b092-120">Указывает имя удобного объекта классификации хранилища, который нужно получить.</span><span class="sxs-lookup"><span data-stu-id="2b092-120">Specifies the friendly name of the storage classification object to get.</span></span>

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

### <span data-ttu-id="2b092-121">-Name</span><span class="sxs-lookup"><span data-stu-id="2b092-121">-Name</span></span>
<span data-ttu-id="2b092-122">Имя объекта классификации хранилища, который нужно получить.</span><span class="sxs-lookup"><span data-stu-id="2b092-122">Specifies the name of the storage classification object to get.</span></span>

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

### <span data-ttu-id="2b092-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b092-123">CommonParameters</span></span>
<span data-ttu-id="2b092-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b092-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b092-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2b092-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b092-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2b092-126">INPUTS</span></span>

### <span data-ttu-id="2b092-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span><span class="sxs-lookup"><span data-stu-id="2b092-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="2b092-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2b092-128">OUTPUTS</span></span>

### <span data-ttu-id="2b092-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="2b092-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="2b092-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2b092-130">NOTES</span></span>

## <span data-ttu-id="2b092-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2b092-131">RELATED LINKS</span></span>
