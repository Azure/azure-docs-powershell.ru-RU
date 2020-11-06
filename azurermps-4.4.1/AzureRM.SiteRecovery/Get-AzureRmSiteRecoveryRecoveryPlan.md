---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 3B879056-5BF3-4262-8BAA-E79589149370
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryRecoveryPlan.md
ms.openlocfilehash: 2d9f087b87d99003b559fc363265fdb4b996c3f9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562095"
---
# <span data-ttu-id="d3383-101">Get-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d3383-101">Get-AzureRmSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="d3383-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d3383-102">SYNOPSIS</span></span>
<span data-ttu-id="d3383-103">Возвращает план восстановления для восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="d3383-103">Gets a recovery plan in Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d3383-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d3383-104">SYNTAX</span></span>

### <span data-ttu-id="d3383-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d3383-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryRecoveryPlan [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d3383-106">ByName</span><span class="sxs-lookup"><span data-stu-id="d3383-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryRecoveryPlan -Name <String> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d3383-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="d3383-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryRecoveryPlan -FriendlyName <String> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3383-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d3383-108">DESCRIPTION</span></span>
<span data-ttu-id="d3383-109">Командлет **Get-AzureRmSiteRecoveryRecoveryPlan** получает план восстановления в Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="d3383-109">The **Get-AzureRmSiteRecoveryRecoveryPlan** cmdlet gets a recovery plan in Azure Site Recovery.</span></span>

## <span data-ttu-id="d3383-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d3383-110">EXAMPLES</span></span>

## <span data-ttu-id="d3383-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d3383-111">PARAMETERS</span></span>

### <span data-ttu-id="d3383-112">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="d3383-112">-FriendlyName</span></span>
<span data-ttu-id="d3383-113">Указывает понятное имя плана восстановления, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="d3383-113">Specifies the friendly name of the recovery plan that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d3383-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d3383-114">-Name</span></span>
<span data-ttu-id="d3383-115">Указывает имя плана восстановления, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="d3383-115">Specifies the name of the recovery plan that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d3383-116">-Path</span><span class="sxs-lookup"><span data-stu-id="d3383-116">-Path</span></span>
<span data-ttu-id="d3383-117">Указывает путь к файлу, в который этот командлет сохраняет план восстановления.</span><span class="sxs-lookup"><span data-stu-id="d3383-117">Specifies the file path to which this cmdlet saves the recovery plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName, ByFriendlyName
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3383-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3383-118">-DefaultProfile</span></span>
<span data-ttu-id="d3383-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d3383-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3383-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3383-120">CommonParameters</span></span>
<span data-ttu-id="d3383-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d3383-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3383-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3383-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3383-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d3383-123">INPUTS</span></span>

## <span data-ttu-id="d3383-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d3383-124">OUTPUTS</span></span>

### <span data-ttu-id="d3383-125">System. Collections. Generic. IEnumerable 1 [Microsoft. Azure. Commands. SiteRecovery. ASRRecoveryPlan]</span><span class="sxs-lookup"><span data-stu-id="d3383-125">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPlan]</span></span>

## <span data-ttu-id="d3383-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="d3383-126">NOTES</span></span>

## <span data-ttu-id="d3383-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d3383-127">RELATED LINKS</span></span>

[<span data-ttu-id="d3383-128">New-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d3383-128">New-AzureRmSiteRecoveryRecoveryPlan</span></span>](./New-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="d3383-129">Remove-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d3383-129">Remove-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Remove-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="d3383-130">Update-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d3383-130">Update-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Update-AzureRmSiteRecoveryRecoveryPlan.md)
