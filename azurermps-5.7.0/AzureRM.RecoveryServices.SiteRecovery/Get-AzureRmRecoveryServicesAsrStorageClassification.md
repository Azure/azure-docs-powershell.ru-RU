---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrstorageclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrStorageClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrStorageClassification.md
ms.openlocfilehash: 8bea83b033ffb8a2e56ba6d28759e88280529a2b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733246"
---
# <span data-ttu-id="13060-101">Get-AzureRmRecoveryServicesAsrStorageClassification</span><span class="sxs-lookup"><span data-stu-id="13060-101">Get-AzureRmRecoveryServicesAsrStorageClassification</span></span>

## <span data-ttu-id="13060-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="13060-102">SYNOPSIS</span></span>
<span data-ttu-id="13060-103">Получает доступные (обнаруженные) классификации хранилища ASR в хранилище служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="13060-103">Gets the available(discovered) ASR storage classifications in the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="13060-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="13060-104">SYNTAX</span></span>

### <span data-ttu-id="13060-105">ByFabricObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="13060-105">ByFabricObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrStorageClassification -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="13060-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="13060-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrStorageClassification -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="13060-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="13060-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrStorageClassification -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13060-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="13060-108">DESCRIPTION</span></span>
<span data-ttu-id="13060-109">Командлет **Get-AzureRmRecoveryServicesAsrStorageClassification** получает сведения о обнаруженных классификациях хранилища ASR в хранилище служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="13060-109">The **Get-AzureRmRecoveryServicesAsrStorageClassification** cmdlet gets details of the discovered ASR storage classifications in the Recovery Services vault.</span></span>

## <span data-ttu-id="13060-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="13060-110">EXAMPLES</span></span>

### <span data-ttu-id="13060-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="13060-111">Example 1</span></span>
```
PS C:\> $StorageClassifications = Get-AzureRmRecoveryServicesAsrStorageClassification -Fabric $Fabric
```

<span data-ttu-id="13060-112">Перечислите обнаруженные классификации хранилища, соответствующие указанной структуре ASR.</span><span class="sxs-lookup"><span data-stu-id="13060-112">List the discovered storage classifications corresponding to the specified ASR fabric.</span></span> 

## <span data-ttu-id="13060-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="13060-113">PARAMETERS</span></span>

### <span data-ttu-id="13060-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13060-114">-DefaultProfile</span></span>
<span data-ttu-id="13060-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="13060-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="13060-116">-Fabric</span><span class="sxs-lookup"><span data-stu-id="13060-116">-Fabric</span></span>
<span data-ttu-id="13060-117">Указывает объект Fabric ASR.</span><span class="sxs-lookup"><span data-stu-id="13060-117">Specifies an ASR fabric object.</span></span> <span data-ttu-id="13060-118">Командлет получает подробные сведения о обнаруженных классификациях хранилища, соответствующих указанной структуре ASR.</span><span class="sxs-lookup"><span data-stu-id="13060-118">The cmdlet gets the details of discovered storage classifications corresponding to the specified ASR fabric.</span></span> 

```yaml
Type: ASRFabric
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="13060-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="13060-119">-FriendlyName</span></span>
<span data-ttu-id="13060-120">Указывает понятное имя объекта классификации хранилища, которое требуется получить.</span><span class="sxs-lookup"><span data-stu-id="13060-120">Specifies the friendly name of the storage classification object to get.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13060-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="13060-121">-Name</span></span>
<span data-ttu-id="13060-122">Указывает имя объекта классификации хранилища, которое требуется получить.</span><span class="sxs-lookup"><span data-stu-id="13060-122">Specifies the name of the storage classification object to get.</span></span>

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

### <span data-ttu-id="13060-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13060-123">CommonParameters</span></span>
<span data-ttu-id="13060-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="13060-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13060-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13060-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13060-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="13060-126">INPUTS</span></span>

### <span data-ttu-id="13060-127">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="13060-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="13060-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="13060-128">OUTPUTS</span></span>

### <span data-ttu-id="13060-129">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRStorageClassification, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="13060-129">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="13060-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="13060-130">NOTES</span></span>

## <span data-ttu-id="13060-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="13060-131">RELATED LINKS</span></span>
