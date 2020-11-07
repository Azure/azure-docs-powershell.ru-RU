---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: 80e5e698183cdba8489f0978c5b34ee7be575140
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93904957"
---
# <span data-ttu-id="0f8f4-101">Get-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="0f8f4-101">Get-AzRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="0f8f4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0f8f4-102">SYNOPSIS</span></span>
<span data-ttu-id="0f8f4-103">Получает сведения о поставщиках служб восстановления ASR, зарегистрированных в хранилище служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="0f8f4-103">Gets the details of the ASR recovery services providers registered to the Recovery Services vault.</span></span>

## <span data-ttu-id="0f8f4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0f8f4-104">SYNTAX</span></span>

### <span data-ttu-id="0f8f4-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0f8f4-105">Default (Default)</span></span>
```
Get-AzRecoveryServicesAsrServicesProvider -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0f8f4-106">ByName</span><span class="sxs-lookup"><span data-stu-id="0f8f4-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrServicesProvider -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0f8f4-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="0f8f4-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrServicesProvider -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f8f4-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0f8f4-108">DESCRIPTION</span></span>
<span data-ttu-id="0f8f4-109">Командлет **Get-AzRecoveryServicesAsrServicesProvider** получает сведения о поставщиках Azure Site Recovery в хранилище.</span><span class="sxs-lookup"><span data-stu-id="0f8f4-109">The **Get-AzRecoveryServicesAsrServicesProvider** cmdlet gets information on the Azure Site Recovery providers in the vault.</span></span>

## <span data-ttu-id="0f8f4-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0f8f4-110">EXAMPLES</span></span>

### <span data-ttu-id="0f8f4-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0f8f4-111">Example 1</span></span>
```
PS C:\> $RSPs = Get-AzRecoveryServicesAsrFabric | Get-AzRecoveryServicesAsrServicesProvider
```

<span data-ttu-id="0f8f4-112">Список всех поставщиков служб репликации ASR, зарегистрированных в хранилище служб восстановления, соответствующем указанной структуре.</span><span class="sxs-lookup"><span data-stu-id="0f8f4-112">List all ASR replication services providers registered to the Recovery Services vault corresponding to the specified fabric.</span></span>

## <span data-ttu-id="0f8f4-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0f8f4-113">PARAMETERS</span></span>

### <span data-ttu-id="0f8f4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f8f4-114">-DefaultProfile</span></span>
<span data-ttu-id="0f8f4-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0f8f4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="0f8f4-116">-Fabric</span><span class="sxs-lookup"><span data-stu-id="0f8f4-116">-Fabric</span></span>
<span data-ttu-id="0f8f4-117">Указывает объект Fabric ASR.</span><span class="sxs-lookup"><span data-stu-id="0f8f4-117">Specifies the ASR fabric object.</span></span>

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

### <span data-ttu-id="0f8f4-118">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="0f8f4-118">-FriendlyName</span></span>
<span data-ttu-id="0f8f4-119">Указывает понятное имя поставщика служб восстановления ASR, для которого требуется получить подробные сведения.</span><span class="sxs-lookup"><span data-stu-id="0f8f4-119">Specifies the friendly name of the ASR recovery services provider to get details for.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f8f4-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0f8f4-120">-Name</span></span>
<span data-ttu-id="0f8f4-121">Указывает имя поставщика служб восстановления ASR, для которого требуется получить подробные сведения.</span><span class="sxs-lookup"><span data-stu-id="0f8f4-121">Specifies the name of the ASR recovery services provider to get details for.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f8f4-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f8f4-122">CommonParameters</span></span>
<span data-ttu-id="0f8f4-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0f8f4-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f8f4-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f8f4-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f8f4-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0f8f4-125">INPUTS</span></span>

### <span data-ttu-id="0f8f4-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="0f8f4-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="0f8f4-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0f8f4-127">OUTPUTS</span></span>

### <span data-ttu-id="0f8f4-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="0f8f4-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="0f8f4-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="0f8f4-129">NOTES</span></span>

## <span data-ttu-id="0f8f4-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0f8f4-130">RELATED LINKS</span></span>

[<span data-ttu-id="0f8f4-131">Remove-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="0f8f4-131">Remove-AzRecoveryServicesAsrServicesProvider</span></span>](./Remove-AzRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="0f8f4-132">Update-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="0f8f4-132">Update-AzRecoveryServicesAsrServicesProvider</span></span>](./Update-AzRecoveryServicesAsrServicesProvider.md)
