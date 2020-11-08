---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrstorageclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassification.md
ms.openlocfilehash: a5265f6c824160ccd06022d54613818131f4da94
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065081"
---
# <span data-ttu-id="2a2c2-101">Get-AzRecoveryServicesAsrStorageClassification</span><span class="sxs-lookup"><span data-stu-id="2a2c2-101">Get-AzRecoveryServicesAsrStorageClassification</span></span>

## <span data-ttu-id="2a2c2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2a2c2-102">SYNOPSIS</span></span>
<span data-ttu-id="2a2c2-103">Получает доступные (обнаруженные) классификации хранилища ASR в хранилище служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="2a2c2-103">Gets the available(discovered) ASR storage classifications in the Recovery Services vault.</span></span>

## <span data-ttu-id="2a2c2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2a2c2-104">SYNTAX</span></span>

### <span data-ttu-id="2a2c2-105">ByFabricObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2a2c2-105">ByFabricObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrStorageClassification -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2a2c2-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="2a2c2-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrStorageClassification -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2a2c2-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="2a2c2-107">ByObjectWithFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrStorageClassification -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2a2c2-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2a2c2-108">DESCRIPTION</span></span>
<span data-ttu-id="2a2c2-109">Командлет **Get-AzRecoveryServicesAsrStorageClassification** получает сведения о обнаруженных классификациях хранилища ASR в хранилище служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="2a2c2-109">The **Get-AzRecoveryServicesAsrStorageClassification** cmdlet gets details of the discovered ASR storage classifications in the Recovery Services vault.</span></span>

## <span data-ttu-id="2a2c2-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2a2c2-110">EXAMPLES</span></span>

### <span data-ttu-id="2a2c2-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2a2c2-111">Example 1</span></span>
```
PS C:\> $StorageClassifications = Get-AzRecoveryServicesAsrStorageClassification -Fabric $Fabric
```

<span data-ttu-id="2a2c2-112">Перечислите обнаруженные классификации хранилища, соответствующие указанной структуре ASR.</span><span class="sxs-lookup"><span data-stu-id="2a2c2-112">List the discovered storage classifications corresponding to the specified ASR fabric.</span></span> 

## <span data-ttu-id="2a2c2-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2a2c2-113">PARAMETERS</span></span>

### <span data-ttu-id="2a2c2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a2c2-114">-DefaultProfile</span></span>
<span data-ttu-id="2a2c2-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2a2c2-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="2a2c2-116">-Fabric</span><span class="sxs-lookup"><span data-stu-id="2a2c2-116">-Fabric</span></span>
<span data-ttu-id="2a2c2-117">Указывает объект Fabric ASR.</span><span class="sxs-lookup"><span data-stu-id="2a2c2-117">Specifies an ASR fabric object.</span></span> <span data-ttu-id="2a2c2-118">Командлет получает подробные сведения о обнаруженных классификациях хранилища, соответствующих указанной структуре ASR.</span><span class="sxs-lookup"><span data-stu-id="2a2c2-118">The cmdlet gets the details of discovered storage classifications corresponding to the specified ASR fabric.</span></span> 

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

### <span data-ttu-id="2a2c2-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="2a2c2-119">-FriendlyName</span></span>
<span data-ttu-id="2a2c2-120">Указывает понятное имя объекта классификации хранилища, которое требуется получить.</span><span class="sxs-lookup"><span data-stu-id="2a2c2-120">Specifies the friendly name of the storage classification object to get.</span></span>

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

### <span data-ttu-id="2a2c2-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2a2c2-121">-Name</span></span>
<span data-ttu-id="2a2c2-122">Указывает имя объекта классификации хранилища, которое требуется получить.</span><span class="sxs-lookup"><span data-stu-id="2a2c2-122">Specifies the name of the storage classification object to get.</span></span>

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

### <span data-ttu-id="2a2c2-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a2c2-123">CommonParameters</span></span>
<span data-ttu-id="2a2c2-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2a2c2-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a2c2-125">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2a2c2-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a2c2-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2a2c2-126">INPUTS</span></span>

### <span data-ttu-id="2a2c2-127">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="2a2c2-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="2a2c2-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2a2c2-128">OUTPUTS</span></span>

### <span data-ttu-id="2a2c2-129">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="2a2c2-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="2a2c2-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="2a2c2-130">NOTES</span></span>

## <span data-ttu-id="2a2c2-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2a2c2-131">RELATED LINKS</span></span>
