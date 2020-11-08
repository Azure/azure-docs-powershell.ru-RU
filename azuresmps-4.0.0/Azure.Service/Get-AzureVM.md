---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: BBA0D5D3-29A5-4E00-9075-702E2F81CA52
online version: ''
schema: 2.0.0
ms.openlocfilehash: bcff7873042d9f7a07eee26f93312c8690e16416
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076547"
---
# <span data-ttu-id="700f2-101">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="700f2-101">Get-AzureVM</span></span>

## <span data-ttu-id="700f2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="700f2-102">SYNOPSIS</span></span>
<span data-ttu-id="700f2-103">Получение сведений из одной или нескольких виртуальных машин Azure.</span><span class="sxs-lookup"><span data-stu-id="700f2-103">Retrieves information from one or more Azure virtual machines.</span></span>

## <span data-ttu-id="700f2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="700f2-104">SYNTAX</span></span>

### <span data-ttu-id="700f2-105">ListAllVMs (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="700f2-105">ListAllVMs (Default)</span></span>
```
Get-AzureVM [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="700f2-106">GetVMByServiceAndVMName</span><span class="sxs-lookup"><span data-stu-id="700f2-106">GetVMByServiceAndVMName</span></span>
```
Get-AzureVM [-ServiceName] <String> [[-Name] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="700f2-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="700f2-107">DESCRIPTION</span></span>
<span data-ttu-id="700f2-108">Командлет **Get-AzureVM** извлекает сведения о виртуальных машинах, работающих в Azure.</span><span class="sxs-lookup"><span data-stu-id="700f2-108">The **Get-AzureVM** cmdlet retrieves information about virtual machines running in Azure.</span></span>
<span data-ttu-id="700f2-109">Он возвращает объект со сведениями о конкретной виртуальной машине или, если виртуальная машина не указана, для всех виртуальных машин в указанной службе текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="700f2-109">It returns an object with information on a specific virtual machine, or if no virtual machine is specified, for all the virtual machines in the specified service of the current subscription.</span></span>

## <span data-ttu-id="700f2-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="700f2-110">EXAMPLES</span></span>

### <span data-ttu-id="700f2-111">Пример 1: получение сведений об указанной виртуальной машине</span><span class="sxs-lookup"><span data-stu-id="700f2-111">Example 1: Retrieve information on a specified virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService01" -Name "VirtualMachine02"
```

<span data-ttu-id="700f2-112">Эта команда возвращает объект со сведениями о виртуальной машине VirtualMachine02, работающей в облачной службе ContosoService01.</span><span class="sxs-lookup"><span data-stu-id="700f2-112">This command returns an object with information on the VirtualMachine02 virtual machine running in the ContosoService01 cloud service.</span></span>

### <span data-ttu-id="700f2-113">Пример 2: получение сведений на всех виртуальных машинах</span><span class="sxs-lookup"><span data-stu-id="700f2-113">Example 2: Retrieve information on all virtual machines</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService01"
```

<span data-ttu-id="700f2-114">Эта команда извлекает объект List со сведениями обо всех виртуальных машинах, запущенных в облачной службе ContosoService01.</span><span class="sxs-lookup"><span data-stu-id="700f2-114">This command retrieves a list object with information on all of the virtual machines running in the ContosoService01 cloud service.</span></span>

### <span data-ttu-id="700f2-115">Пример 3: отображение таблицы состояния виртуальных машин</span><span class="sxs-lookup"><span data-stu-id="700f2-115">Example 3: Display a table of virtual machine statuses</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService01"  | Format-Table AutoSize -Property "Name",@{Expression={$_.InstanceUpgradeDomain};Label="UpgDom";Align="Right"},"InstanceStatus"
```

<span data-ttu-id="700f2-116">Эта команда отображает таблицу, в которой показаны виртуальные машины, запущенные в службе ContosoService01, их домен обновления, а также текущее состояние каждой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="700f2-116">This command displays a table showing the virtual machines running on the ContosoService01 service, their Upgrade Domain, and the current status of each virtual machine.</span></span>

## <span data-ttu-id="700f2-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="700f2-117">PARAMETERS</span></span>

### <span data-ttu-id="700f2-118">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="700f2-118">-InformationAction</span></span>
<span data-ttu-id="700f2-119">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="700f2-119">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="700f2-120">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="700f2-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="700f2-121">Продолжал</span><span class="sxs-lookup"><span data-stu-id="700f2-121">Continue</span></span>
- <span data-ttu-id="700f2-122">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="700f2-122">Ignore</span></span>
- <span data-ttu-id="700f2-123">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="700f2-123">Inquire</span></span>
- <span data-ttu-id="700f2-124">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="700f2-124">SilentlyContinue</span></span>
- <span data-ttu-id="700f2-125">Остановить</span><span class="sxs-lookup"><span data-stu-id="700f2-125">Stop</span></span>
- <span data-ttu-id="700f2-126">Рвать</span><span class="sxs-lookup"><span data-stu-id="700f2-126">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="700f2-127">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="700f2-127">-InformationVariable</span></span>
<span data-ttu-id="700f2-128">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="700f2-128">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="700f2-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="700f2-129">-Name</span></span>
<span data-ttu-id="700f2-130">Указывает имя виртуальной машины, для которой требуется получить сведения.</span><span class="sxs-lookup"><span data-stu-id="700f2-130">Specifies the name of the virtual machine for which to retrieve information.</span></span>
<span data-ttu-id="700f2-131">Если этот параметр не указан, командлет возвращает объект List со сведениями обо всех виртуальных машинах в указанной службе.</span><span class="sxs-lookup"><span data-stu-id="700f2-131">If this parameter is not provided, the cmdlet returns a list object with information about all the virtual machines in the specified service.</span></span>

```yaml
Type: String
Parameter Sets: GetVMByServiceAndVMName
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="700f2-132">-Profile</span><span class="sxs-lookup"><span data-stu-id="700f2-132">-Profile</span></span>
<span data-ttu-id="700f2-133">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="700f2-133">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="700f2-134">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="700f2-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="700f2-135">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="700f2-135">-ServiceName</span></span>
<span data-ttu-id="700f2-136">Указывает имя облачной службы, для которой требуется возвратить сведения о виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="700f2-136">Specifies the name of the cloud service for which to return virtual machine information.</span></span>

```yaml
Type: String
Parameter Sets: GetVMByServiceAndVMName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="700f2-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="700f2-137">CommonParameters</span></span>
<span data-ttu-id="700f2-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="700f2-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="700f2-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="700f2-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="700f2-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="700f2-140">INPUTS</span></span>

## <span data-ttu-id="700f2-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="700f2-141">OUTPUTS</span></span>

## <span data-ttu-id="700f2-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="700f2-142">NOTES</span></span>

## <span data-ttu-id="700f2-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="700f2-143">RELATED LINKS</span></span>

[<span data-ttu-id="700f2-144">New-AzureVM</span><span class="sxs-lookup"><span data-stu-id="700f2-144">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="700f2-145">New-AzureVMConfig</span><span class="sxs-lookup"><span data-stu-id="700f2-145">New-AzureVMConfig</span></span>](./New-AzureVMConfig.md)

[<span data-ttu-id="700f2-146">Remove-AzureVM</span><span class="sxs-lookup"><span data-stu-id="700f2-146">Remove-AzureVM</span></span>](./Remove-AzureVM.md)

[<span data-ttu-id="700f2-147">Restarts-AzureVM</span><span class="sxs-lookup"><span data-stu-id="700f2-147">Restart-AzureVM</span></span>](./Restart-AzureVM.md)

[<span data-ttu-id="700f2-148">Start-AzureVM</span><span class="sxs-lookup"><span data-stu-id="700f2-148">Start-AzureVM</span></span>](./Start-AzureVM.md)

[<span data-ttu-id="700f2-149">Stop-AzureVM</span><span class="sxs-lookup"><span data-stu-id="700f2-149">Stop-AzureVM</span></span>](./Stop-AzureVM.md)

[<span data-ttu-id="700f2-150">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="700f2-150">Update-AzureVM</span></span>](./Update-AzureVM.md)


