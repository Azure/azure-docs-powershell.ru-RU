---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: 4be24acddf1f02ecd9216a06690958feed2d6c57
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065078"
---
# <span data-ttu-id="2d88d-101">Get-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="2d88d-101">Get-AzRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="2d88d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2d88d-102">SYNOPSIS</span></span>
<span data-ttu-id="2d88d-103">Получает сведения о поставщиках служб восстановления ASR, зарегистрированных в хранилище служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="2d88d-103">Gets the details of the ASR recovery services providers registered to the Recovery Services vault.</span></span>

## <span data-ttu-id="2d88d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2d88d-104">SYNTAX</span></span>

### <span data-ttu-id="2d88d-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2d88d-105">Default (Default)</span></span>
```
Get-AzRecoveryServicesAsrServicesProvider -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2d88d-106">ByName</span><span class="sxs-lookup"><span data-stu-id="2d88d-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrServicesProvider -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2d88d-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="2d88d-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrServicesProvider -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2d88d-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2d88d-108">DESCRIPTION</span></span>
<span data-ttu-id="2d88d-109">Командлет **Get-AzRecoveryServicesAsrServicesProvider** получает сведения о поставщиках Azure Site Recovery в хранилище.</span><span class="sxs-lookup"><span data-stu-id="2d88d-109">The **Get-AzRecoveryServicesAsrServicesProvider** cmdlet gets information on the Azure Site Recovery providers in the vault.</span></span>

## <span data-ttu-id="2d88d-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2d88d-110">EXAMPLES</span></span>

### <span data-ttu-id="2d88d-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2d88d-111">Example 1</span></span>
```
PS C:\> $RSPs = Get-AzRecoveryServicesAsrFabric | Get-AzRecoveryServicesAsrServicesProvider
```

<span data-ttu-id="2d88d-112">Список всех поставщиков служб репликации ASR, зарегистрированных в хранилище служб восстановления, соответствующем указанной структуре.</span><span class="sxs-lookup"><span data-stu-id="2d88d-112">List all ASR replication services providers registered to the Recovery Services vault corresponding to the specified fabric.</span></span>

## <span data-ttu-id="2d88d-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2d88d-113">PARAMETERS</span></span>

### <span data-ttu-id="2d88d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d88d-114">-DefaultProfile</span></span>
<span data-ttu-id="2d88d-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2d88d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="2d88d-116">-Fabric</span><span class="sxs-lookup"><span data-stu-id="2d88d-116">-Fabric</span></span>
<span data-ttu-id="2d88d-117">Указывает объект Fabric ASR.</span><span class="sxs-lookup"><span data-stu-id="2d88d-117">Specifies the ASR fabric object.</span></span>

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

### <span data-ttu-id="2d88d-118">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="2d88d-118">-FriendlyName</span></span>
<span data-ttu-id="2d88d-119">Указывает понятное имя поставщика служб восстановления ASR, для которого требуется получить подробные сведения.</span><span class="sxs-lookup"><span data-stu-id="2d88d-119">Specifies the friendly name of the ASR recovery services provider to get details for.</span></span>

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

### <span data-ttu-id="2d88d-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2d88d-120">-Name</span></span>
<span data-ttu-id="2d88d-121">Указывает имя поставщика служб восстановления ASR, для которого требуется получить подробные сведения.</span><span class="sxs-lookup"><span data-stu-id="2d88d-121">Specifies the name of the ASR recovery services provider to get details for.</span></span>

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

### <span data-ttu-id="2d88d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d88d-122">CommonParameters</span></span>
<span data-ttu-id="2d88d-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2d88d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d88d-124">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2d88d-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d88d-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2d88d-125">INPUTS</span></span>

### <span data-ttu-id="2d88d-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="2d88d-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="2d88d-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2d88d-127">OUTPUTS</span></span>

### <span data-ttu-id="2d88d-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="2d88d-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="2d88d-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="2d88d-129">NOTES</span></span>

## <span data-ttu-id="2d88d-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2d88d-130">RELATED LINKS</span></span>

[<span data-ttu-id="2d88d-131">Remove-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="2d88d-131">Remove-AzRecoveryServicesAsrServicesProvider</span></span>](./Remove-AzRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="2d88d-132">Update-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="2d88d-132">Update-AzRecoveryServicesAsrServicesProvider</span></span>](./Update-AzRecoveryServicesAsrServicesProvider.md)
