---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: F6C01C25-655C-4798-9826-F7CB168181C7
online version: ''
schema: 2.0.0
ms.openlocfilehash: bc8b7dc7e23a98111e75c2b2c9c079f010e3c5dc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075590"
---
# <span data-ttu-id="5e031-101">Get-AzureSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="5e031-101">Get-AzureSiteRecoveryNetworkMapping</span></span>

## <span data-ttu-id="5e031-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5e031-102">SYNOPSIS</span></span>
<span data-ttu-id="5e031-103">Получение сетевых сопоставлений для хранилища сайтов восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="5e031-103">Gets network mappings for a Site Recovery vault.</span></span>

## <span data-ttu-id="5e031-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5e031-104">SYNTAX</span></span>

### <span data-ttu-id="5e031-105">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="5e031-105">EnterpriseToEnterprise</span></span>
```
Get-AzureSiteRecoveryNetworkMapping -PrimaryServer <ASRServer> -RecoveryServer <ASRServer>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="5e031-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="5e031-106">EnterpriseToAzure</span></span>
```
Get-AzureSiteRecoveryNetworkMapping -PrimaryServer <ASRServer> [-Azure] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="5e031-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5e031-107">DESCRIPTION</span></span>
<span data-ttu-id="5e031-108">Командлет **Get-AzureSiteRecoveryNetworkMapping** получает сведения о сопоставлениях сети Azure Site Recovery для текущего хранилища сайта для восстановления.</span><span class="sxs-lookup"><span data-stu-id="5e031-108">The **Get-AzureSiteRecoveryNetworkMapping** cmdlet gets information about Azure Site Recovery network mappings for the current Site Recovery vault.</span></span>

## <span data-ttu-id="5e031-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5e031-109">EXAMPLES</span></span>

### <span data-ttu-id="5e031-110">Пример 1: получение сопоставления между сетью и сетью восстановления</span><span class="sxs-lookup"><span data-stu-id="5e031-110">Example 1: Get the mapping between a network and a recovery network</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> Get-AzureSiteRecoveryNetworkMapping -PrimaryServer $Servers[0] -RecoveryServer $Servers[0]
PrimaryServerId     : 774859b0-1966-48cc-9df7-759c441b7a8c
PrimaryNetworkId    : 7cfd636e-5cc2-4e01-873b-8a7aa4962341
PrimaryNetworkName  : phase2RecoveryVMNetwork
RecoveryServerId    : 774859b0-1966-48cc-9df7-759c441b7a8c
RecoveryNetworkId   : d903e2c6-3141-4cef-bfe1-04616cd43cbb
RecoveryNetworkName : phase2PrimaryVMNetwork
PairingStatus       : OK
```

<span data-ttu-id="5e031-111">Первый командлет команды получает серверы для текущего хранилища Azure Site Recovery с помощью командлета **Get-AzureSiteRecoveryServer** .</span><span class="sxs-lookup"><span data-stu-id="5e031-111">The first command cmdlet gets servers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>
<span data-ttu-id="5e031-112">Команда хранит серверы восстановления сайта в переменной массива $Servers.</span><span class="sxs-lookup"><span data-stu-id="5e031-112">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="5e031-113">Вторая команда получает сопоставление между основной сетью и сетью восстановления.</span><span class="sxs-lookup"><span data-stu-id="5e031-113">The second command gets the mapping between the primary network and the recovery network.</span></span>
<span data-ttu-id="5e031-114">Команда задает основной сервер для сетевого сопоставления в качестве первого элемента $Servers.</span><span class="sxs-lookup"><span data-stu-id="5e031-114">The command specifies the primary server for the network mapping as the first element of $Servers.</span></span>
<span data-ttu-id="5e031-115">Команда задает сервер для сети восстановления во втором элементе $Servers.</span><span class="sxs-lookup"><span data-stu-id="5e031-115">The command specifies the server for the recovery network as the second element of $Servers.</span></span>

### <span data-ttu-id="5e031-116">Пример 2: получение сопоставления между сетью и сетью виртуальных машин Azure</span><span class="sxs-lookup"><span data-stu-id="5e031-116">Example 2: Get the mapping between a network and an Azure virtual machine network</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> Get-AzureSiteRecoveryNetworkMapping -Azure -PrimaryServer $Servers[0] 
PrimaryServerId     : 774859b0-1966-48cc-9df7-759c441b7a8c
PrimaryNetworkId    : 7cfd636e-5cc2-4e01-873b-8a7aa4962341
PrimaryNetworkName  : phase2RecoveryVMNetwork
RecoveryServerId    : 21a9403c-6ec1-44f2-b744-b4e50b792387
RecoveryNetworkId   : ecb3a462-664f-4f57-873e-d09b5925e1a1
RecoveryNetworkName : AzureVMNetwork
PairingStatus       : OK
```

<span data-ttu-id="5e031-117">Первый командлет команды получает серверы для текущего хранилища для восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="5e031-117">The first command cmdlet gets servers for the current Site Recovery vault.</span></span>
<span data-ttu-id="5e031-118">Команда хранит серверы в переменной массива $Servers.</span><span class="sxs-lookup"><span data-stu-id="5e031-118">The command stores the servers in the $Servers array variable.</span></span>

<span data-ttu-id="5e031-119">Вторая команда получает сопоставление между основной сетью и сетью виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="5e031-119">The second command gets a mapping between the primary network and an Azure virtual machine network.</span></span>
<span data-ttu-id="5e031-120">Команда задает основной сервер для сети в качестве первого элемента $Servers.</span><span class="sxs-lookup"><span data-stu-id="5e031-120">The command specifies the primary server for the network as the first element of $Servers.</span></span>
<span data-ttu-id="5e031-121">Команда задает параметр *Azure* .</span><span class="sxs-lookup"><span data-stu-id="5e031-121">The command specifies the *Azure* parameter.</span></span>
<span data-ttu-id="5e031-122">Таким образом, команда получает сопоставление с сетью виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="5e031-122">Therefore, the command gets the mapping to an Azure virtual machine network.</span></span>

## <span data-ttu-id="5e031-123">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5e031-123">PARAMETERS</span></span>

### <span data-ttu-id="5e031-124">-Azure</span><span class="sxs-lookup"><span data-stu-id="5e031-124">-Azure</span></span>
<span data-ttu-id="5e031-125">Указывает на то, что этот командлет получает сетевые сопоставления для сетей на основном сервере, сопоставленных с виртуальными сетями Azure.</span><span class="sxs-lookup"><span data-stu-id="5e031-125">Indicates that this cmdlet gets network mappings for networks on the primary server mapped to Azure virtual networks.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e031-126">-PrimaryServer</span><span class="sxs-lookup"><span data-stu-id="5e031-126">-PrimaryServer</span></span>
<span data-ttu-id="5e031-127">Указывает основной сервер, для которого нужно получить сопоставления.</span><span class="sxs-lookup"><span data-stu-id="5e031-127">Specifies a primary server for which to get mappings.</span></span>

```yaml
Type: ASRServer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e031-128">-Profile</span><span class="sxs-lookup"><span data-stu-id="5e031-128">-Profile</span></span>
<span data-ttu-id="5e031-129">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="5e031-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5e031-130">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5e031-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5e031-131">-RecoveryServer</span><span class="sxs-lookup"><span data-stu-id="5e031-131">-RecoveryServer</span></span>
<span data-ttu-id="5e031-132">Указывает сервер восстановления, для которого требуется получить сопоставления.</span><span class="sxs-lookup"><span data-stu-id="5e031-132">Specifies a recovery server for which to get mappings.</span></span>

```yaml
Type: ASRServer
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e031-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e031-133">CommonParameters</span></span>
<span data-ttu-id="5e031-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5e031-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e031-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e031-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e031-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5e031-136">INPUTS</span></span>

## <span data-ttu-id="5e031-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5e031-137">OUTPUTS</span></span>

## <span data-ttu-id="5e031-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="5e031-138">NOTES</span></span>

## <span data-ttu-id="5e031-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5e031-139">RELATED LINKS</span></span>

[<span data-ttu-id="5e031-140">New-AzureSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="5e031-140">New-AzureSiteRecoveryNetworkMapping</span></span>](./New-AzureSiteRecoveryNetworkMapping.md)

[<span data-ttu-id="5e031-141">Remove-AzureSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="5e031-141">Remove-AzureSiteRecoveryNetworkMapping</span></span>](./Remove-AzureSiteRecoveryNetworkMapping.md)


