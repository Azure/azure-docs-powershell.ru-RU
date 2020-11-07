---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrstorageclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassification.md
ms.openlocfilehash: 9f0021658784c767e35d903a0a191ba28932f57a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729721"
---
# <span data-ttu-id="5296d-101">Get-AzRecoveryServicesAsrStorageClassification</span><span class="sxs-lookup"><span data-stu-id="5296d-101">Get-AzRecoveryServicesAsrStorageClassification</span></span>

## <span data-ttu-id="5296d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5296d-102">SYNOPSIS</span></span>
<span data-ttu-id="5296d-103">Получает доступные (обнаруженные) классификации хранилища ASR в хранилище служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="5296d-103">Gets the available(discovered) ASR storage classifications in the Recovery Services vault.</span></span>

## <span data-ttu-id="5296d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5296d-104">SYNTAX</span></span>

### <span data-ttu-id="5296d-105">ByFabricObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5296d-105">ByFabricObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrStorageClassification -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5296d-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="5296d-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrStorageClassification -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5296d-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="5296d-107">ByObjectWithFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrStorageClassification -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5296d-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5296d-108">DESCRIPTION</span></span>
<span data-ttu-id="5296d-109">Командлет **Get-AzRecoveryServicesAsrStorageClassification** получает сведения о обнаруженных классификациях хранилища ASR в хранилище служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="5296d-109">The **Get-AzRecoveryServicesAsrStorageClassification** cmdlet gets details of the discovered ASR storage classifications in the Recovery Services vault.</span></span>

## <span data-ttu-id="5296d-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5296d-110">EXAMPLES</span></span>

### <span data-ttu-id="5296d-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5296d-111">Example 1</span></span>
```
PS C:\> $StorageClassifications = Get-AzRecoveryServicesAsrStorageClassification -Fabric $Fabric
```

<span data-ttu-id="5296d-112">Перечислите обнаруженные классификации хранилища, соответствующие указанной структуре ASR.</span><span class="sxs-lookup"><span data-stu-id="5296d-112">List the discovered storage classifications corresponding to the specified ASR fabric.</span></span> 

## <span data-ttu-id="5296d-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5296d-113">PARAMETERS</span></span>

### <span data-ttu-id="5296d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5296d-114">-DefaultProfile</span></span>
<span data-ttu-id="5296d-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5296d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="5296d-116">-Fabric</span><span class="sxs-lookup"><span data-stu-id="5296d-116">-Fabric</span></span>
<span data-ttu-id="5296d-117">Указывает объект Fabric ASR.</span><span class="sxs-lookup"><span data-stu-id="5296d-117">Specifies an ASR fabric object.</span></span> <span data-ttu-id="5296d-118">Командлет получает подробные сведения о обнаруженных классификациях хранилища, соответствующих указанной структуре ASR.</span><span class="sxs-lookup"><span data-stu-id="5296d-118">The cmdlet gets the details of discovered storage classifications corresponding to the specified ASR fabric.</span></span> 

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

### <span data-ttu-id="5296d-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="5296d-119">-FriendlyName</span></span>
<span data-ttu-id="5296d-120">Указывает понятное имя объекта классификации хранилища, которое требуется получить.</span><span class="sxs-lookup"><span data-stu-id="5296d-120">Specifies the friendly name of the storage classification object to get.</span></span>

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

### <span data-ttu-id="5296d-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5296d-121">-Name</span></span>
<span data-ttu-id="5296d-122">Указывает имя объекта классификации хранилища, которое требуется получить.</span><span class="sxs-lookup"><span data-stu-id="5296d-122">Specifies the name of the storage classification object to get.</span></span>

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

### <span data-ttu-id="5296d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5296d-123">CommonParameters</span></span>
<span data-ttu-id="5296d-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5296d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5296d-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5296d-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5296d-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5296d-126">INPUTS</span></span>

### <span data-ttu-id="5296d-127">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="5296d-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="5296d-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5296d-128">OUTPUTS</span></span>

### <span data-ttu-id="5296d-129">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="5296d-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="5296d-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="5296d-130">NOTES</span></span>

## <span data-ttu-id="5296d-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5296d-131">RELATED LINKS</span></span>
