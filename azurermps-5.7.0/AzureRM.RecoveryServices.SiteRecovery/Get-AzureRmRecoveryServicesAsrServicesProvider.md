---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: 3eb55379b84570ad49bbea038b4264345508c82c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732518"
---
# <span data-ttu-id="adabe-101">Get-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="adabe-101">Get-AzureRmRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="adabe-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="adabe-102">SYNOPSIS</span></span>
<span data-ttu-id="adabe-103">Получает сведения о поставщиках служб восстановления ASR, зарегистрированных в хранилище служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="adabe-103">Gets the details of the ASR recovery services providers registered to the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="adabe-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="adabe-104">SYNTAX</span></span>

### <span data-ttu-id="adabe-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="adabe-105">Default (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrServicesProvider -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="adabe-106">ByName</span><span class="sxs-lookup"><span data-stu-id="adabe-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrServicesProvider -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="adabe-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="adabe-107">ByFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrServicesProvider -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="adabe-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="adabe-108">DESCRIPTION</span></span>
<span data-ttu-id="adabe-109">Командлет **Get-AzureRmRecoveryServicesAsrServicesProvider** получает сведения о поставщиках Azure Site Recovery в хранилище.</span><span class="sxs-lookup"><span data-stu-id="adabe-109">The **Get-AzureRmRecoveryServicesAsrServicesProvider** cmdlet gets information on the Azure Site Recovery providers in the vault.</span></span>

## <span data-ttu-id="adabe-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="adabe-110">EXAMPLES</span></span>

### <span data-ttu-id="adabe-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="adabe-111">Example 1</span></span>
```
PS C:\> $RSPs = Get-AzureRmRecoveryServicesAsrFabric | Get-AzureRmRecoveryServicesAsrServicesProvider
```

<span data-ttu-id="adabe-112">Список всех поставщиков служб репликации ASR, зарегистрированных в хранилище служб восстановления, соответствующем указанной структуре.</span><span class="sxs-lookup"><span data-stu-id="adabe-112">List all ASR replication services providers registered to the Recovery Services vault corresponding to the specified fabric.</span></span>

## <span data-ttu-id="adabe-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="adabe-113">PARAMETERS</span></span>

### <span data-ttu-id="adabe-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adabe-114">-DefaultProfile</span></span>
<span data-ttu-id="adabe-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="adabe-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="adabe-116">-Fabric</span><span class="sxs-lookup"><span data-stu-id="adabe-116">-Fabric</span></span>
<span data-ttu-id="adabe-117">Указывает объект Fabric ASR.</span><span class="sxs-lookup"><span data-stu-id="adabe-117">Specifies the ASR fabric object.</span></span>

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

### <span data-ttu-id="adabe-118">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="adabe-118">-FriendlyName</span></span>
<span data-ttu-id="adabe-119">Указывает понятное имя поставщика служб восстановления ASR, для которого требуется получить подробные сведения.</span><span class="sxs-lookup"><span data-stu-id="adabe-119">Specifies the friendly name of the ASR recovery services provider to get details for.</span></span>

```yaml
Type: String
Parameter Sets: ByFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adabe-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="adabe-120">-Name</span></span>
<span data-ttu-id="adabe-121">Указывает имя поставщика служб восстановления ASR, для которого требуется получить подробные сведения.</span><span class="sxs-lookup"><span data-stu-id="adabe-121">Specifies the name of the ASR recovery services provider to get details for.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adabe-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adabe-122">CommonParameters</span></span>
<span data-ttu-id="adabe-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="adabe-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adabe-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="adabe-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adabe-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="adabe-125">INPUTS</span></span>

### <span data-ttu-id="adabe-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="adabe-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="adabe-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="adabe-127">OUTPUTS</span></span>

### <span data-ttu-id="adabe-128">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryServicesProvider, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="adabe-128">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="adabe-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="adabe-129">NOTES</span></span>

## <span data-ttu-id="adabe-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="adabe-130">RELATED LINKS</span></span>

[<span data-ttu-id="adabe-131">Remove-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="adabe-131">Remove-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Remove-AzureRmRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="adabe-132">Update-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="adabe-132">Update-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Update-AzureRmRecoveryServicesAsrServicesProvider.md)
