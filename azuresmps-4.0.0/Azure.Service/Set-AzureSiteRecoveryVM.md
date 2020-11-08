---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 30D56D40-2EA0-48D1-846A-AFB4A987E08F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9dac9858a251e0390fd2a11a2c01dddede1613b5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075754"
---
# <span data-ttu-id="e4722-101">Set-AzureSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="e4722-101">Set-AzureSiteRecoveryVM</span></span>

## <span data-ttu-id="e4722-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e4722-102">SYNOPSIS</span></span>
<span data-ttu-id="e4722-103">Задает параметры на стороне восстановления для объекта защиты восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="e4722-103">Sets the recovery-side options for a Site Recovery protection entity.</span></span>

## <span data-ttu-id="e4722-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e4722-104">SYNTAX</span></span>

```
Set-AzureSiteRecoveryVM -VirtualMachine <ASRVirtualMachine> [-Name <String>] [-Size <String>]
 [-PrimaryNic <String>] [-RecoveryNetworkId <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e4722-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e4722-105">DESCRIPTION</span></span>
<span data-ttu-id="e4722-106">Командлет **Set-AzureSiteRecoveryVM** задает параметры защиты на стороне восстановления, такие как размер виртуальной машины восстановления и сеть виртуальных машин для восстановления, для сущностей защита Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="e4722-106">The **Set-AzureSiteRecoveryVM** cmdlet sets the recovery-side protection options, such as the recovery virtual machine size and recovery virtual machine network, for Azure Site Recovery protection entities.</span></span>

## <span data-ttu-id="e4722-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e4722-107">EXAMPLES</span></span>

### <span data-ttu-id="e4722-108">Пример 1: разрешение обновления на защищенной виртуальной машине</span><span class="sxs-lookup"><span data-stu-id="e4722-108">Example 1: Allow the update on a protected virtual machine</span></span>
```
PS C:\> $ProtectionContainer = Get-AzureSiteRecoveryProtectionContainer
PS C:\> $VirtualMachines = Get-AzureSiteRecoveryVM -ProtectionContainer $ProtectionContainer 
PS C:\> Set-AzureSiteRecoveryVM -VirtualMachine $VirtualMachines[0] -Name "NewVirtualMachine05"
Name             : 
ID               : 8170d274-1e48-404a-b080-172ada140bc3
ClientRequestId  : 09354052-8430-4fa8-9a35-63196dd4b2b4-2015-02-03 04:19:06Z-P
State            : NotStarted
StateDescription : NotStarted
StartTime        : 
EndTime          : 
AllowedActions   : 
Tasks            : {}
Errors           : {}
```

<span data-ttu-id="e4722-109">Первая команда использует командлет **Get-AzureSiteRecoveryProtectionContainer** для получения защищенного контейнера и сохраняет его в переменной $ProtectionContainer.</span><span class="sxs-lookup"><span data-stu-id="e4722-109">The first command uses the **Get-AzureSiteRecoveryProtectionContainer** cmdlet to get a protected container, and then stores it in the $ProtectionContainer variable.</span></span>

<span data-ttu-id="e4722-110">Вторая команда получает виртуальные машины в $ProtectionContainer с помощью командлета **Get-AzureSiteRecoveryVM** , а затем сохраняет их в переменной $VitrualMachines.</span><span class="sxs-lookup"><span data-stu-id="e4722-110">The second command gets the virtual machines in $ProtectionContainer, by using the **Get-AzureSiteRecoveryVM** cmdlet, and then stores them in the $VitrualMachines variable.</span></span>

<span data-ttu-id="e4722-111">Последняя команда позволяет обновления для первой виртуальной машины в массиве $VitrualMachines с именем NewVirtualMachine05.</span><span class="sxs-lookup"><span data-stu-id="e4722-111">The final command allows updates for the first virtual machine in the $VitrualMachines array, named NewVirtualMachine05.</span></span>

## <span data-ttu-id="e4722-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e4722-112">PARAMETERS</span></span>

### <span data-ttu-id="e4722-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e4722-113">-Name</span></span>
<span data-ttu-id="e4722-114">Указывает имя целевой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e4722-114">Specifies the name of the target virtual machine.</span></span>

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

### <span data-ttu-id="e4722-115">-PrimaryNic</span><span class="sxs-lookup"><span data-stu-id="e4722-115">-PrimaryNic</span></span>
<span data-ttu-id="e4722-116">Задает основной адаптер сетевого адаптера.</span><span class="sxs-lookup"><span data-stu-id="e4722-116">Specifies the primary network adapter card.</span></span>

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

### <span data-ttu-id="e4722-117">-Profile</span><span class="sxs-lookup"><span data-stu-id="e4722-117">-Profile</span></span>
<span data-ttu-id="e4722-118">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="e4722-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e4722-119">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e4722-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e4722-120">-RecoveryNetworkId</span><span class="sxs-lookup"><span data-stu-id="e4722-120">-RecoveryNetworkId</span></span>
<span data-ttu-id="e4722-121">Указывает ИД сети восстановления.</span><span class="sxs-lookup"><span data-stu-id="e4722-121">Specifies the recovery network ID.</span></span>

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

### <span data-ttu-id="e4722-122">-Size</span><span class="sxs-lookup"><span data-stu-id="e4722-122">-Size</span></span>
<span data-ttu-id="e4722-123">Указывает целевой размер виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e4722-123">Specifies the target virtual machine size.</span></span>

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

### <span data-ttu-id="e4722-124">-VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="e4722-124">-VirtualMachine</span></span>
<span data-ttu-id="e4722-125">Указывает объект виртуальной машины для восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="e4722-125">Specifies the Site Recovery virtual machine object.</span></span>

```yaml
Type: ASRVirtualMachine
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4722-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4722-126">CommonParameters</span></span>
<span data-ttu-id="e4722-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e4722-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4722-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4722-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4722-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e4722-129">INPUTS</span></span>

## <span data-ttu-id="e4722-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e4722-130">OUTPUTS</span></span>

## <span data-ttu-id="e4722-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="e4722-131">NOTES</span></span>

## <span data-ttu-id="e4722-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e4722-132">RELATED LINKS</span></span>

[<span data-ttu-id="e4722-133">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="e4722-133">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="e4722-134">Get-AzureSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="e4722-134">Get-AzureSiteRecoveryVM</span></span>](./Get-AzureSiteRecoveryVM.md)


