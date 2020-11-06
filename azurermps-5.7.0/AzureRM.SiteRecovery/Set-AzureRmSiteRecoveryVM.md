---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 483D4C1A-D34E-40ED-B92B-82187FF321F7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/set-azurermsiterecoveryvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryVM.md
ms.openlocfilehash: b330cb59281a3f140ba30f10f31ecb5bf3b49f97
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567879"
---
# <span data-ttu-id="b9446-101">Set-AzureRmSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="b9446-101">Set-AzureRmSiteRecoveryVM</span></span>

## <span data-ttu-id="b9446-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b9446-102">SYNOPSIS</span></span>
<span data-ttu-id="b9446-103">Задает параметры на стороне восстановления для объекта защиты восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="b9446-103">Sets the recovery-side options for a Site Recovery protection entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b9446-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b9446-104">SYNTAX</span></span>

```
Set-AzureRmSiteRecoveryVM -VirtualMachine <ASRVirtualMachine> [-Name <String>] [-Size <String>]
 [-PrimaryNic <String>] [-RecoveryNetworkId <String>] [-RecoveryNicSubnetName <String>]
 [-RecoveryNicStaticIPAddress <String>] [-NicSelectionType <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b9446-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b9446-105">DESCRIPTION</span></span>
<span data-ttu-id="b9446-106">Командлет **Set-AzureRmSiteRecoveryVM** задает параметры защиты на стороне восстановления, такие как размер виртуальной машины восстановления и сеть виртуальных машин для восстановления, для сущностей защита Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="b9446-106">The **Set-AzureRmSiteRecoveryVM** cmdlet sets the recovery-side protection options, such as the recovery virtual machine size and recovery virtual machine network, for Azure Site Recovery protection entities.</span></span>

## <span data-ttu-id="b9446-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b9446-107">EXAMPLES</span></span>

## <span data-ttu-id="b9446-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b9446-108">PARAMETERS</span></span>

### <span data-ttu-id="b9446-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9446-109">-DefaultProfile</span></span>
<span data-ttu-id="b9446-110">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b9446-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b9446-111">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b9446-111">-Name</span></span>
<span data-ttu-id="b9446-112">Указывает имя целевой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="b9446-112">Specifies the name of the target virtual machine.</span></span>

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

### <span data-ttu-id="b9446-113">-NicSelectionType</span><span class="sxs-lookup"><span data-stu-id="b9446-113">-NicSelectionType</span></span>
<span data-ttu-id="b9446-114">Задает свойства выбор сетевого адаптера.</span><span class="sxs-lookup"><span data-stu-id="b9446-114">Specifies the network adapter selection properties.</span></span>
<span data-ttu-id="b9446-115">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="b9446-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b9446-116">NotSelected</span><span class="sxs-lookup"><span data-stu-id="b9446-116">NotSelected</span></span>
- <span data-ttu-id="b9446-117">SelectedByUser</span><span class="sxs-lookup"><span data-stu-id="b9446-117">SelectedByUser</span></span>

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

### <span data-ttu-id="b9446-118">-PrimaryNic</span><span class="sxs-lookup"><span data-stu-id="b9446-118">-PrimaryNic</span></span>
<span data-ttu-id="b9446-119">Задает основной адаптер сетевого адаптера.</span><span class="sxs-lookup"><span data-stu-id="b9446-119">Specifies the primary network adapter card.</span></span>

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

### <span data-ttu-id="b9446-120">-RecoveryNetworkId</span><span class="sxs-lookup"><span data-stu-id="b9446-120">-RecoveryNetworkId</span></span>
<span data-ttu-id="b9446-121">Указывает ИД сети восстановления.</span><span class="sxs-lookup"><span data-stu-id="b9446-121">Specifies the recovery network ID.</span></span>

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

### <span data-ttu-id="b9446-122">-RecoveryNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="b9446-122">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="b9446-123">Статический IP-адрес, назначенный контроллеру основного сетевого адаптера при восстановлении.</span><span class="sxs-lookup"><span data-stu-id="b9446-123">Specifies the static IP address that is assigned to primary network adapter controller on recovery.</span></span>

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

### <span data-ttu-id="b9446-124">-RecoveryNicSubnetName</span><span class="sxs-lookup"><span data-stu-id="b9446-124">-RecoveryNicSubnetName</span></span>
<span data-ttu-id="b9446-125">Указывает имя подсети виртуальной сети Azure, к которому нужно присоединить основной контроллер сетевого адаптера при восстановлении.</span><span class="sxs-lookup"><span data-stu-id="b9446-125">Specifies the Azure virtual network subnet name with which to attach the primary network adapter controller on recovery.</span></span>

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

### <span data-ttu-id="b9446-126">-Size</span><span class="sxs-lookup"><span data-stu-id="b9446-126">-Size</span></span>
<span data-ttu-id="b9446-127">Указывает целевой размер виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="b9446-127">Specifies the target virtual machine size.</span></span>

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

### <span data-ttu-id="b9446-128">-VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="b9446-128">-VirtualMachine</span></span>
<span data-ttu-id="b9446-129">Указывает объект виртуальной машины для восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="b9446-129">Specifies the Site Recovery virtual machine object.</span></span>

```yaml
Type: ASRVirtualMachine
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b9446-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9446-130">CommonParameters</span></span>
<span data-ttu-id="b9446-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b9446-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9446-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9446-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9446-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b9446-133">INPUTS</span></span>

### <span data-ttu-id="b9446-134">ASRVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="b9446-134">ASRVirtualMachine</span></span>
<span data-ttu-id="b9446-135">Параметр "VirtualMachine" принимает значение типа "ASRVirtualMachine" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="b9446-135">Parameter 'VirtualMachine' accepts value of type 'ASRVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="b9446-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b9446-136">OUTPUTS</span></span>

### <span data-ttu-id="b9446-137">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="b9446-137">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="b9446-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="b9446-138">NOTES</span></span>

## <span data-ttu-id="b9446-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b9446-139">RELATED LINKS</span></span>

[<span data-ttu-id="b9446-140">Get-AzureRmSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="b9446-140">Get-AzureRmSiteRecoveryVM</span></span>](./Get-AzureRmSiteRecoveryVM.md)
