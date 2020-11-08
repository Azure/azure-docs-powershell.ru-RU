---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: BB36A434-6BE3-46BF-B10A-FCD6C766CB84
online version: ''
schema: 2.0.0
ms.openlocfilehash: 87414a56778123053615bb36a06113e2b0b0633f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076110"
---
# <span data-ttu-id="a7b13-101">Remove-AzureSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="a7b13-101">Remove-AzureSiteRecoveryNetworkMapping</span></span>

## <span data-ttu-id="a7b13-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a7b13-102">SYNOPSIS</span></span>
<span data-ttu-id="a7b13-103">Удаляет Сетевое сопоставление из хранилища сайта.</span><span class="sxs-lookup"><span data-stu-id="a7b13-103">Removes a network mapping from a Site Recovery vault.</span></span>

## <span data-ttu-id="a7b13-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a7b13-104">SYNTAX</span></span>

```
Remove-AzureSiteRecoveryNetworkMapping -NetworkMapping <ASRNetworkMapping> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="a7b13-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a7b13-105">DESCRIPTION</span></span>
<span data-ttu-id="a7b13-106">Командлет **Remove-AzureSiteRecoveryNetworkMapping** удаляет Сетевое сопоставление из текущего хранилища Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="a7b13-106">The **Remove-AzureSiteRecoveryNetworkMapping** cmdlet removes a network mapping from the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="a7b13-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a7b13-107">EXAMPLES</span></span>

### <span data-ttu-id="a7b13-108">Пример 1: Удаление сопоставления между сетью и сетью восстановления</span><span class="sxs-lookup"><span data-stu-id="a7b13-108">Example 1: Remove the mapping between a network and a recovery network</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> $NetworkMapping = Get-AzureSiteRecoveryNetworkMapping -PrimaryServer $Servers[0] -RecoveryServer $Servers[0]
PS C:\> Remove-AzureSiteRecoveryNetworkMapping -NetworkMapping $NetworkMapping
```

<span data-ttu-id="a7b13-109">Первый командлет команды получает серверы для текущего хранилища Azure Site Recovery с помощью командлета **Get-AzureSiteRecoveryServer** .</span><span class="sxs-lookup"><span data-stu-id="a7b13-109">The first command cmdlet gets servers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>
<span data-ttu-id="a7b13-110">Команда хранит серверы восстановления сайта в переменной массива $Servers.</span><span class="sxs-lookup"><span data-stu-id="a7b13-110">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="a7b13-111">Вторая команда получает сопоставление между основной сетью и сетью восстановления, а затем сохраняет его в переменной $NetworkMapping.</span><span class="sxs-lookup"><span data-stu-id="a7b13-111">The second command gets the mapping between the primary network and the recovery network, and then stores it in the $NetworkMapping variable.</span></span>
<span data-ttu-id="a7b13-112">Команда задает основной сервер для сетевого сопоставления в качестве первого элемента $Servers.</span><span class="sxs-lookup"><span data-stu-id="a7b13-112">The command specifies the primary server for the network mapping as the first element of $Servers.</span></span>
<span data-ttu-id="a7b13-113">Команда задает сервер для сети восстановления во втором элементе $Servers.</span><span class="sxs-lookup"><span data-stu-id="a7b13-113">The command specifies the server for the recovery network as the second element of $Servers.</span></span>

<span data-ttu-id="a7b13-114">Последняя команда удаляет Сетевое сопоставление в $NetworkMapping.</span><span class="sxs-lookup"><span data-stu-id="a7b13-114">The final command removes the network mapping in $NetworkMapping.</span></span>

### <span data-ttu-id="a7b13-115">Пример 2: Удаление сопоставления сети и сети виртуальной машины Azure</span><span class="sxs-lookup"><span data-stu-id="a7b13-115">Example 2: Remove the mapping between a network and an Azure virtual machine network</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> $NetworkMapping = Get-AzureSiteRecoveryNetworkMapping -PrimaryServer $Servers[0] -Azure
PS C:\> Remove-AzureSiteRecoveryNetworkMapping -NetworkMapping $NetworkMapping
```

<span data-ttu-id="a7b13-116">Первый командлет команды получает серверы для текущего хранилища для восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="a7b13-116">The first command cmdlet gets servers for the current Site Recovery vault.</span></span>
<span data-ttu-id="a7b13-117">Команда хранит серверы восстановления сайта в переменной массива $Servers.</span><span class="sxs-lookup"><span data-stu-id="a7b13-117">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="a7b13-118">Вторая команда получает сопоставление между основной сетью и сетью виртуальной машины Azure, а затем сохраняет его в переменной $NetworkMapping.</span><span class="sxs-lookup"><span data-stu-id="a7b13-118">The second command gets a mapping between the primary network and an Azure virtual machine network, and then stores it in the $NetworkMapping variable.</span></span>
<span data-ttu-id="a7b13-119">Команда задает основной сервер для сети в качестве первого элемента $Servers.</span><span class="sxs-lookup"><span data-stu-id="a7b13-119">The command specifies the primary server for the network as the first element of $Servers.</span></span>
<span data-ttu-id="a7b13-120">Команда задает параметр *Azure* .</span><span class="sxs-lookup"><span data-stu-id="a7b13-120">The command specifies the *Azure* parameter.</span></span>
<span data-ttu-id="a7b13-121">Таким образом, команда получает сопоставление с сетью виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="a7b13-121">Therefore, the command gets the mapping to an Azure virtual machine network.</span></span>

<span data-ttu-id="a7b13-122">Последняя команда удаляет Сетевое сопоставление в $NetworkMapping.</span><span class="sxs-lookup"><span data-stu-id="a7b13-122">The final command removes the network mapping in $NetworkMapping.</span></span>

## <span data-ttu-id="a7b13-123">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a7b13-123">PARAMETERS</span></span>

### <span data-ttu-id="a7b13-124">-NetworkMapping</span><span class="sxs-lookup"><span data-stu-id="a7b13-124">-NetworkMapping</span></span>
<span data-ttu-id="a7b13-125">Указывает сетевое сопоставление для удаления.</span><span class="sxs-lookup"><span data-stu-id="a7b13-125">Specifies the network mapping to remove.</span></span>

```yaml
Type: ASRNetworkMapping
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a7b13-126">-Profile</span><span class="sxs-lookup"><span data-stu-id="a7b13-126">-Profile</span></span>
<span data-ttu-id="a7b13-127">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a7b13-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a7b13-128">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a7b13-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a7b13-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7b13-129">CommonParameters</span></span>
<span data-ttu-id="a7b13-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a7b13-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7b13-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7b13-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7b13-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a7b13-132">INPUTS</span></span>

## <span data-ttu-id="a7b13-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a7b13-133">OUTPUTS</span></span>

## <span data-ttu-id="a7b13-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="a7b13-134">NOTES</span></span>

## <span data-ttu-id="a7b13-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a7b13-135">RELATED LINKS</span></span>

[<span data-ttu-id="a7b13-136">Get-AzureSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="a7b13-136">Get-AzureSiteRecoveryNetworkMapping</span></span>](./Get-AzureSiteRecoveryNetworkMapping.md)

[<span data-ttu-id="a7b13-137">New-AzureSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="a7b13-137">New-AzureSiteRecoveryNetworkMapping</span></span>](./New-AzureSiteRecoveryNetworkMapping.md)

[<span data-ttu-id="a7b13-138">Get-AzureSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="a7b13-138">Get-AzureSiteRecoveryServer</span></span>](./Get-AzureSiteRecoveryServer.md)


