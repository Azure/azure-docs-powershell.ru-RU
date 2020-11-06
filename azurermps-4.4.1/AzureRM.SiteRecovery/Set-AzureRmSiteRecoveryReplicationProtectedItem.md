---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: FCE4633A-4F75-4A23-B825-6AC62238658A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryReplicationProtectedItem.md
ms.openlocfilehash: 2070a26a1bfdb41e5135479548f04bdbaced6884
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562087"
---
# <span data-ttu-id="1975d-101">Set-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="1975d-101">Set-AzureRmSiteRecoveryReplicationProtectedItem</span></span>

## <span data-ttu-id="1975d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1975d-102">SYNOPSIS</span></span>
<span data-ttu-id="1975d-103">Задает свойства восстановления, такие как Целевая сеть и размер виртуальной машины, для элемента, защищенного репликацией.</span><span class="sxs-lookup"><span data-stu-id="1975d-103">Sets recovery properties such as target network and virtual machine size for a Replication Protected Item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1975d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1975d-104">SYNTAX</span></span>

```
Set-AzureRmSiteRecoveryReplicationProtectedItem -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-Name <String>] [-Size <String>] [-PrimaryNic <String>] [-RecoveryNetworkId <String>]
 [-RecoveryNicSubnetName <String>] [-RecoveryNicStaticIPAddress <String>] [-NicSelectionType <String>]
 [-LicenseType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1975d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1975d-105">DESCRIPTION</span></span>
<span data-ttu-id="1975d-106">Командлет **Set-AzureRmSiteRecoveryReplicationProtectedItem** задает свойства восстановления для элемента, защищенного репликацией.</span><span class="sxs-lookup"><span data-stu-id="1975d-106">The **Set-AzureRmSiteRecoveryReplicationProtectedItem** cmdlet sets the recovery properties for a Replication Protected Item.</span></span>

## <span data-ttu-id="1975d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1975d-107">EXAMPLES</span></span>

## <span data-ttu-id="1975d-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1975d-108">PARAMETERS</span></span>

### <span data-ttu-id="1975d-109">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="1975d-109">-LicenseType</span></span>
<span data-ttu-id="1975d-110">Указывает тип лицензии для виртуальных машин Windows Server, перенесенных с помощью гибридного использования преимуществ.</span><span class="sxs-lookup"><span data-stu-id="1975d-110">Specifies the license type selection for Windows Server virtual machines migrated through Hybrid use benefit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: NoLicenseType, WindowsServer

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1975d-111">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1975d-111">-Name</span></span>
<span data-ttu-id="1975d-112">Указывает имя виртуальной машины восстановления.</span><span class="sxs-lookup"><span data-stu-id="1975d-112">Specifies the name of the recovery virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1975d-113">-NicSelectionType</span><span class="sxs-lookup"><span data-stu-id="1975d-113">-NicSelectionType</span></span>
<span data-ttu-id="1975d-114">Задает свойства сетевого адаптера, заданные пользователем или заданные по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1975d-114">Specifies the network interface card (NIC) properties set by user or set by default.</span></span>
<span data-ttu-id="1975d-115">Вы можете указать NotSelected, чтобы вернуться к значениям по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1975d-115">You can specify NotSelected to go back to the default values.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: NotSelected, SelectedByUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1975d-116">-PrimaryNic</span><span class="sxs-lookup"><span data-stu-id="1975d-116">-PrimaryNic</span></span>
<span data-ttu-id="1975d-117">Задает сетевую карту виртуальной машины, для которой этот командлет задает свойство сетевого восстановления.</span><span class="sxs-lookup"><span data-stu-id="1975d-117">Specifies the NIC of the virtual machine for which this cmdlet sets the recovery network property.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1975d-118">-RecoveryNetworkId</span><span class="sxs-lookup"><span data-stu-id="1975d-118">-RecoveryNetworkId</span></span>
<span data-ttu-id="1975d-119">Указывает идентификатор виртуальной сети Azure, для которой этот командлет подлежит защищенному элементу.</span><span class="sxs-lookup"><span data-stu-id="1975d-119">Specifies the ID of the Azure virtual network for which this cmdlet recovers the Protected Item.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1975d-120">-RecoveryNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="1975d-120">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="1975d-121">Статический IP-адрес, который должен быть назначен основной NIC при восстановлении.</span><span class="sxs-lookup"><span data-stu-id="1975d-121">Specifies the static IP address that should be assigned to primary NIC on recovery.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1975d-122">-RecoveryNicSubnetName</span><span class="sxs-lookup"><span data-stu-id="1975d-122">-RecoveryNicSubnetName</span></span>
<span data-ttu-id="1975d-123">Имя подсети в виртуальной сети Azure, для которой этот командлет восопределяет защищенный элемент.</span><span class="sxs-lookup"><span data-stu-id="1975d-123">Specifies the name of the Subnet on the recovery Azure virtual network for which this cmdlet recovers the Protected Item.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1975d-124">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="1975d-124">-ReplicationProtectedItem</span></span>
<span data-ttu-id="1975d-125">Задает защищенный элемент репликации Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="1975d-125">Specifies the Azure Site Recovery Replication Protected Item.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1975d-126">-Size</span><span class="sxs-lookup"><span data-stu-id="1975d-126">-Size</span></span>
<span data-ttu-id="1975d-127">Указывает размер виртуальной машины для восстановления.</span><span class="sxs-lookup"><span data-stu-id="1975d-127">Specifies the recovery virtual machine size.</span></span>
<span data-ttu-id="1975d-128">Значение должно быть из набора размеров, поддерживаемых виртуальными машинами Azure.</span><span class="sxs-lookup"><span data-stu-id="1975d-128">The value should be from the set of sizes supported by Azure virtual machines.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1975d-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1975d-129">-DefaultProfile</span></span>
<span data-ttu-id="1975d-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1975d-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1975d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1975d-131">CommonParameters</span></span>
<span data-ttu-id="1975d-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1975d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1975d-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1975d-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1975d-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1975d-134">INPUTS</span></span>

### <span data-ttu-id="1975d-135">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="1975d-135">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="1975d-136">Параметр "ReplicationProtectedItem" принимает значение типа "ASRReplicationProtectedItem" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="1975d-136">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="1975d-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1975d-137">OUTPUTS</span></span>

### <span data-ttu-id="1975d-138">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="1975d-138">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="1975d-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="1975d-139">NOTES</span></span>

## <span data-ttu-id="1975d-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1975d-140">RELATED LINKS</span></span>

[<span data-ttu-id="1975d-141">Get-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="1975d-141">Get-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Get-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="1975d-142">New-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="1975d-142">New-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./New-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="1975d-143">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="1975d-143">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Remove-AzureRmSiteRecoveryReplicationProtectedItem.md)
