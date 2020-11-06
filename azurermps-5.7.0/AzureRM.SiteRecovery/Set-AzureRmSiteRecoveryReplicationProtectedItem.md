---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: FCE4633A-4F75-4A23-B825-6AC62238658A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/set-azurermsiterecoveryreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryReplicationProtectedItem.md
ms.openlocfilehash: e09cc216b7ba3ef383467ea53478cfe8819e0a4c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567881"
---
# <span data-ttu-id="af8d9-101">Set-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="af8d9-101">Set-AzureRmSiteRecoveryReplicationProtectedItem</span></span>

## <span data-ttu-id="af8d9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="af8d9-102">SYNOPSIS</span></span>
<span data-ttu-id="af8d9-103">Задает свойства восстановления, такие как Целевая сеть и размер виртуальной машины, для элемента, защищенного репликацией.</span><span class="sxs-lookup"><span data-stu-id="af8d9-103">Sets recovery properties such as target network and virtual machine size for a Replication Protected Item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af8d9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="af8d9-104">SYNTAX</span></span>

```
Set-AzureRmSiteRecoveryReplicationProtectedItem -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-Name <String>] [-Size <String>] [-PrimaryNic <String>] [-RecoveryNetworkId <String>]
 [-RecoveryNicSubnetName <String>] [-RecoveryNicStaticIPAddress <String>] [-NicSelectionType <String>]
 [-LicenseType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af8d9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="af8d9-105">DESCRIPTION</span></span>
<span data-ttu-id="af8d9-106">Командлет **Set-AzureRmSiteRecoveryReplicationProtectedItem** задает свойства восстановления для элемента, защищенного репликацией.</span><span class="sxs-lookup"><span data-stu-id="af8d9-106">The **Set-AzureRmSiteRecoveryReplicationProtectedItem** cmdlet sets the recovery properties for a Replication Protected Item.</span></span>

## <span data-ttu-id="af8d9-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="af8d9-107">EXAMPLES</span></span>

## <span data-ttu-id="af8d9-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="af8d9-108">PARAMETERS</span></span>

### <span data-ttu-id="af8d9-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af8d9-109">-DefaultProfile</span></span>
<span data-ttu-id="af8d9-110">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="af8d9-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="af8d9-111">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="af8d9-111">-LicenseType</span></span>
<span data-ttu-id="af8d9-112">Указывает тип лицензии для виртуальных машин Windows Server, перенесенных с помощью гибридного использования преимуществ.</span><span class="sxs-lookup"><span data-stu-id="af8d9-112">Specifies the license type selection for Windows Server virtual machines migrated through Hybrid use benefit.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: NoLicenseType, WindowsServer

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af8d9-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="af8d9-113">-Name</span></span>
<span data-ttu-id="af8d9-114">Указывает имя виртуальной машины восстановления.</span><span class="sxs-lookup"><span data-stu-id="af8d9-114">Specifies the name of the recovery virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af8d9-115">-NicSelectionType</span><span class="sxs-lookup"><span data-stu-id="af8d9-115">-NicSelectionType</span></span>
<span data-ttu-id="af8d9-116">Задает свойства сетевого адаптера, заданные пользователем или заданные по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="af8d9-116">Specifies the network interface card (NIC) properties set by user or set by default.</span></span>
<span data-ttu-id="af8d9-117">Вы можете указать NotSelected, чтобы вернуться к значениям по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="af8d9-117">You can specify NotSelected to go back to the default values.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: NotSelected, SelectedByUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af8d9-118">-PrimaryNic</span><span class="sxs-lookup"><span data-stu-id="af8d9-118">-PrimaryNic</span></span>
<span data-ttu-id="af8d9-119">Задает сетевую карту виртуальной машины, для которой этот командлет задает свойство сетевого восстановления.</span><span class="sxs-lookup"><span data-stu-id="af8d9-119">Specifies the NIC of the virtual machine for which this cmdlet sets the recovery network property.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af8d9-120">-RecoveryNetworkId</span><span class="sxs-lookup"><span data-stu-id="af8d9-120">-RecoveryNetworkId</span></span>
<span data-ttu-id="af8d9-121">Указывает идентификатор виртуальной сети Azure, для которой этот командлет подлежит защищенному элементу.</span><span class="sxs-lookup"><span data-stu-id="af8d9-121">Specifies the ID of the Azure virtual network for which this cmdlet recovers the Protected Item.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af8d9-122">-RecoveryNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="af8d9-122">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="af8d9-123">Статический IP-адрес, который должен быть назначен основной NIC при восстановлении.</span><span class="sxs-lookup"><span data-stu-id="af8d9-123">Specifies the static IP address that should be assigned to primary NIC on recovery.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af8d9-124">-RecoveryNicSubnetName</span><span class="sxs-lookup"><span data-stu-id="af8d9-124">-RecoveryNicSubnetName</span></span>
<span data-ttu-id="af8d9-125">Имя подсети в виртуальной сети Azure, для которой этот командлет восопределяет защищенный элемент.</span><span class="sxs-lookup"><span data-stu-id="af8d9-125">Specifies the name of the Subnet on the recovery Azure virtual network for which this cmdlet recovers the Protected Item.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af8d9-126">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="af8d9-126">-ReplicationProtectedItem</span></span>
<span data-ttu-id="af8d9-127">Задает защищенный элемент репликации Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="af8d9-127">Specifies the Azure Site Recovery Replication Protected Item.</span></span>

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

### <span data-ttu-id="af8d9-128">-Size</span><span class="sxs-lookup"><span data-stu-id="af8d9-128">-Size</span></span>
<span data-ttu-id="af8d9-129">Указывает размер виртуальной машины для восстановления.</span><span class="sxs-lookup"><span data-stu-id="af8d9-129">Specifies the recovery virtual machine size.</span></span>
<span data-ttu-id="af8d9-130">Значение должно быть из набора размеров, поддерживаемых виртуальными машинами Azure.</span><span class="sxs-lookup"><span data-stu-id="af8d9-130">The value should be from the set of sizes supported by Azure virtual machines.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af8d9-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af8d9-131">CommonParameters</span></span>
<span data-ttu-id="af8d9-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="af8d9-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af8d9-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af8d9-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af8d9-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="af8d9-134">INPUTS</span></span>

### <span data-ttu-id="af8d9-135">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="af8d9-135">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="af8d9-136">Параметр "ReplicationProtectedItem" принимает значение типа "ASRReplicationProtectedItem" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="af8d9-136">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="af8d9-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="af8d9-137">OUTPUTS</span></span>

### <span data-ttu-id="af8d9-138">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="af8d9-138">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="af8d9-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="af8d9-139">NOTES</span></span>

## <span data-ttu-id="af8d9-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="af8d9-140">RELATED LINKS</span></span>

[<span data-ttu-id="af8d9-141">Get-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="af8d9-141">Get-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Get-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="af8d9-142">New-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="af8d9-142">New-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./New-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="af8d9-143">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="af8d9-143">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Remove-AzureRmSiteRecoveryReplicationProtectedItem.md)
