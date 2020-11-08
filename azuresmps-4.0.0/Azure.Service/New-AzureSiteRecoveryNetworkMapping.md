---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 6802F2E9-5925-4E92-AEB8-827B5A303617
online version: ''
schema: 2.0.0
ms.openlocfilehash: 153e30c03de7a0a5c404526bd06b9acb2f0678f3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076217"
---
# <span data-ttu-id="5a8bf-101">New-AzureSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="5a8bf-101">New-AzureSiteRecoveryNetworkMapping</span></span>

## <span data-ttu-id="5a8bf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5a8bf-102">SYNOPSIS</span></span>
<span data-ttu-id="5a8bf-103">Создание сопоставления между виртуальными сетями.</span><span class="sxs-lookup"><span data-stu-id="5a8bf-103">Creates a mapping between virtual networks.</span></span>

## <span data-ttu-id="5a8bf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5a8bf-104">SYNTAX</span></span>

### <span data-ttu-id="5a8bf-105">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="5a8bf-105">EnterpriseToEnterprise</span></span>
```
New-AzureSiteRecoveryNetworkMapping -PrimaryNetwork <ASRNetwork> -RecoveryNetwork <ASRNetwork>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="5a8bf-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="5a8bf-106">EnterpriseToAzure</span></span>
```
New-AzureSiteRecoveryNetworkMapping -PrimaryNetwork <ASRNetwork> -AzureSubscriptionId <String>
 -AzureVMNetworkId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="5a8bf-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5a8bf-107">DESCRIPTION</span></span>
<span data-ttu-id="5a8bf-108">Командлет **New-AzureSiteRecoveryNetworkMapping** создает сопоставление между двумя виртуальными сетями и возвращает задание Azure Site Recovery для отслеживания.</span><span class="sxs-lookup"><span data-stu-id="5a8bf-108">The **New-AzureSiteRecoveryNetworkMapping** cmdlet creates a mapping between two virtual networks and returns an Azure Site Recovery job to track it.</span></span>

## <span data-ttu-id="5a8bf-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5a8bf-109">EXAMPLES</span></span>

### <span data-ttu-id="5a8bf-110">Пример 1: Создание сопоставления между сетью и сетью восстановления</span><span class="sxs-lookup"><span data-stu-id="5a8bf-110">Example 1: Create a mapping between a network and a recovery network</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> $Networks = Get-AzureSiteRecoveryNetwork -Server $Servers[0]
PS C:\> New-AzureSiteRecoveryNetworkMapping -PrimaryNetwork $Networks[0] -RecoveryNetwork $Networks[1]
```

<span data-ttu-id="5a8bf-111">Первый командлет команды получает серверы для текущего хранилища Azure Site Recovery с помощью командлета **Get-AzureSiteRecoveryServer** .</span><span class="sxs-lookup"><span data-stu-id="5a8bf-111">The first command cmdlet gets servers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>
<span data-ttu-id="5a8bf-112">Команда хранит серверы восстановления сайта в переменной массива $Servers.</span><span class="sxs-lookup"><span data-stu-id="5a8bf-112">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="5a8bf-113">Вторая команда получает сеть восстановления сайта для первого сервера в массиве $Servers с помощью командлета **Get-AzureSiteRecoveryNetwork** .</span><span class="sxs-lookup"><span data-stu-id="5a8bf-113">The second command gets the site recovery network for the first server in the $Servers array by using the **Get-AzureSiteRecoveryNetwork** cmdlet.</span></span>
<span data-ttu-id="5a8bf-114">Команда хранит сети в переменной $Networks.</span><span class="sxs-lookup"><span data-stu-id="5a8bf-114">The command stores the networks in the $Networks variable.</span></span>

<span data-ttu-id="5a8bf-115">Последняя команда создает сопоставление между основной сетью и сетью восстановления.</span><span class="sxs-lookup"><span data-stu-id="5a8bf-115">The final command creates a mapping between the primary network and the recovery network.</span></span>
<span data-ttu-id="5a8bf-116">Команда задает основную сеть в качестве первого элемента $Networks.</span><span class="sxs-lookup"><span data-stu-id="5a8bf-116">The command specifies the primary network as the first element of $Networks.</span></span>
<span data-ttu-id="5a8bf-117">Команда задает сеть восстановления в качестве второго элемента $Networks.</span><span class="sxs-lookup"><span data-stu-id="5a8bf-117">The command specifies the recovery network as the second element of $Networks.</span></span>

## <span data-ttu-id="5a8bf-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5a8bf-118">PARAMETERS</span></span>

### <span data-ttu-id="5a8bf-119">-AzureSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5a8bf-119">-AzureSubscriptionId</span></span>
<span data-ttu-id="5a8bf-120">Указывает идентификатор подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="5a8bf-120">Specifies the ID of your Azure subscription.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a8bf-121">-AzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="5a8bf-121">-AzureVMNetworkId</span></span>
<span data-ttu-id="5a8bf-122">Указывает идентификатор виртуальной сети Azure.</span><span class="sxs-lookup"><span data-stu-id="5a8bf-122">Specifies the Azure virtual network ID.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a8bf-123">-PrimaryNetwork</span><span class="sxs-lookup"><span data-stu-id="5a8bf-123">-PrimaryNetwork</span></span>
<span data-ttu-id="5a8bf-124">Указывает основной объект сети.</span><span class="sxs-lookup"><span data-stu-id="5a8bf-124">Specifies the primary network object.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a8bf-125">-Profile</span><span class="sxs-lookup"><span data-stu-id="5a8bf-125">-Profile</span></span>
<span data-ttu-id="5a8bf-126">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="5a8bf-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5a8bf-127">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5a8bf-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a8bf-128">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="5a8bf-128">-RecoveryNetwork</span></span>
<span data-ttu-id="5a8bf-129">Указывает сетевой объект для восстановления.</span><span class="sxs-lookup"><span data-stu-id="5a8bf-129">Specifies the recovery network object.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a8bf-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a8bf-130">CommonParameters</span></span>
<span data-ttu-id="5a8bf-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5a8bf-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a8bf-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a8bf-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a8bf-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5a8bf-133">INPUTS</span></span>

## <span data-ttu-id="5a8bf-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5a8bf-134">OUTPUTS</span></span>

## <span data-ttu-id="5a8bf-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="5a8bf-135">NOTES</span></span>

## <span data-ttu-id="5a8bf-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5a8bf-136">RELATED LINKS</span></span>

[<span data-ttu-id="5a8bf-137">Get-AzureSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="5a8bf-137">Get-AzureSiteRecoveryNetworkMapping</span></span>](./Get-AzureSiteRecoveryNetworkMapping.md)

[<span data-ttu-id="5a8bf-138">Get-AzureSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="5a8bf-138">Get-AzureSiteRecoveryServer</span></span>](./Get-AzureSiteRecoveryServer.md)

[<span data-ttu-id="5a8bf-139">Remove-AzureSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="5a8bf-139">Remove-AzureSiteRecoveryNetworkMapping</span></span>](./Remove-AzureSiteRecoveryNetworkMapping.md)


