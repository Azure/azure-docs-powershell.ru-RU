---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 77AFEF57-A4ED-4F82-A3FF-0E33D7810B3B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryrecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryRecoveryPoint.md
ms.openlocfilehash: 42a0a96a32bf1b7f556ee2787f43a5777afa1115
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567905"
---
# <span data-ttu-id="908a6-101">Get-AzureRmSiteRecoveryRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="908a6-101">Get-AzureRmSiteRecoveryRecoveryPoint</span></span>

## <span data-ttu-id="908a6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="908a6-102">SYNOPSIS</span></span>
<span data-ttu-id="908a6-103">Получает доступные точки восстановления для элемента, защищенного репликацией.</span><span class="sxs-lookup"><span data-stu-id="908a6-103">Gets available recovery points for a replication protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="908a6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="908a6-104">SYNTAX</span></span>

### <span data-ttu-id="908a6-105">ByObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="908a6-105">ByObject (Default)</span></span>
```
Get-AzureRmSiteRecoveryRecoveryPoint -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="908a6-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="908a6-106">ByObjectWithName</span></span>
```
Get-AzureRmSiteRecoveryRecoveryPoint -Name <String> -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="908a6-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="908a6-107">DESCRIPTION</span></span>
<span data-ttu-id="908a6-108">Командлет **Get-AzureRmSiteRecoveryRecoveryPoint** получает список доступных точек восстановления для элемента, защищенного репликацией.</span><span class="sxs-lookup"><span data-stu-id="908a6-108">The **Get-AzureRmSiteRecoveryRecoveryPoint** cmdlet gets the list of available recovery points for a replication protected item.</span></span>

## <span data-ttu-id="908a6-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="908a6-109">EXAMPLES</span></span>

## <span data-ttu-id="908a6-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="908a6-110">PARAMETERS</span></span>

### <span data-ttu-id="908a6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="908a6-111">-DefaultProfile</span></span>
<span data-ttu-id="908a6-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="908a6-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="908a6-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="908a6-113">-Name</span></span>
<span data-ttu-id="908a6-114">Указывает имя точки восстановления, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="908a6-114">Specifies the name of the recovery point this cmdlet gets.</span></span>

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

### <span data-ttu-id="908a6-115">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="908a6-115">-ReplicationProtectedItem</span></span>
<span data-ttu-id="908a6-116">Указывает объект защищенного элемента для репликации Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="908a6-116">Specifies the Azure Site Recovery Replication Protected Item object.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="908a6-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="908a6-117">CommonParameters</span></span>
<span data-ttu-id="908a6-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="908a6-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="908a6-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="908a6-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="908a6-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="908a6-120">INPUTS</span></span>

### <span data-ttu-id="908a6-121">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="908a6-121">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="908a6-122">Параметр "ReplicationProtectedItem" принимает значение типа "ASRReplicationProtectedItem" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="908a6-122">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="908a6-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="908a6-123">OUTPUTS</span></span>

### <span data-ttu-id="908a6-124">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. SiteRecovery. ASRRecoveryPoint, Microsoft. Azure. Commands. SiteRecovery, Version = 2.0.1.0, культура = нейтральная, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="908a6-124">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPoint, Microsoft.Azure.Commands.SiteRecovery, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="908a6-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="908a6-125">NOTES</span></span>

## <span data-ttu-id="908a6-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="908a6-126">RELATED LINKS</span></span>

[<span data-ttu-id="908a6-127">Edit-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="908a6-127">Edit-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Edit-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="908a6-128">Get-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="908a6-128">Get-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Get-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="908a6-129">New-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="908a6-129">New-AzureRmSiteRecoveryRecoveryPlan</span></span>](./New-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="908a6-130">Remove-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="908a6-130">Remove-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Remove-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="908a6-131">Update-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="908a6-131">Update-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Update-AzureRmSiteRecoveryRecoveryPlan.md)
