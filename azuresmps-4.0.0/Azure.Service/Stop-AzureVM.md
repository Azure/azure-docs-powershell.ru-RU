---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 4F347DD1-907C-47DB-8F1D-636DE031A56A
online version: ''
schema: 2.0.0
ms.openlocfilehash: e01265cf3db8a0dc3fd9d74a4a263a20965b10fb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075741"
---
# <span data-ttu-id="0972b-101">Stop-AzureVM</span><span class="sxs-lookup"><span data-stu-id="0972b-101">Stop-AzureVM</span></span>

## <span data-ttu-id="0972b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0972b-102">SYNOPSIS</span></span>
<span data-ttu-id="0972b-103">Завершает работу виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="0972b-103">Shuts down an Azure virtual machine.</span></span>

## <span data-ttu-id="0972b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0972b-104">SYNTAX</span></span>

### <span data-ttu-id="0972b-105">ByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0972b-105">ByName (Default)</span></span>
```
Stop-AzureVM [-Name] <String[]> [-StayProvisioned] [-Force] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="0972b-106">Вводим</span><span class="sxs-lookup"><span data-stu-id="0972b-106">Input</span></span>
```
Stop-AzureVM -VM <IPersistentVM[]> [-StayProvisioned] [-Force] [-ServiceName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="0972b-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0972b-107">DESCRIPTION</span></span>
<span data-ttu-id="0972b-108">Командлет **Stop-AzureVM** завершает работу виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="0972b-108">The **Stop-AzureVM** cmdlet shuts down a virtual machine.</span></span>

## <span data-ttu-id="0972b-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0972b-109">EXAMPLES</span></span>

### <span data-ttu-id="0972b-110">Пример 1: отключение виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="0972b-110">Example 1: Shut down a virtual machine</span></span>
```
PS C:\> Stop-AzureVM -ServiceName "ContosoService01" -Name "MyVM"
```

<span data-ttu-id="0972b-111">Эта команда завершает работу виртуальной машины, в которой находится указанная служба.</span><span class="sxs-lookup"><span data-stu-id="0972b-111">This command shuts down a virtual machine that the specified service contains.</span></span>

### <span data-ttu-id="0972b-112">Пример 2: отключение виртуальной машины с помощью объекта виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="0972b-112">Example 2: Shut down a virtual machine by using a virtual machine object</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService01" -Name "MyVM" | Stop-AzureVM
```

<span data-ttu-id="0972b-113">Эта команда завершает работу виртуальной машины, в которой находится указанная служба, с помощью объекта виртуальной машины, возвращаемого функцией **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="0972b-113">This command shuts down a virtual machine that the specified service contains, by using the virtual machine object that **Get-AzureVM** returns.</span></span>

### <span data-ttu-id="0972b-114">Пример 3: отключение виртуальной машины и сохранение подготовленной виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="0972b-114">Example 3: Shut down a VM and keep the VM provisioned</span></span>
```
PS C:\> Stop-AzureVM -ServiceName "ContosoService01" -Name "MyVM" -StayProvisioned
```

<span data-ttu-id="0972b-115">Эта команда завершает работу виртуальной машины, содержащей указанную службу, и сохраняет ее подготовленную.</span><span class="sxs-lookup"><span data-stu-id="0972b-115">This command shuts down a virtual machine that the specified service contains, and keeps it provisioned.</span></span>

### <span data-ttu-id="0972b-116">Пример 4: отключение виртуальной машины и разрешение освобождения последней виртуальной машины в развертывании</span><span class="sxs-lookup"><span data-stu-id="0972b-116">Example 4: Shut down a VM and allow deallocation of the last VM in the deployment</span></span>
```
PS C:\> Stop-AzureVM -ServiceName "ContosoService01" -Name "MyVM" -Force
```

<span data-ttu-id="0972b-117">Эта команда завершает работу виртуальной машины, в которой находится указанная служба, и позволяет выделять последнюю виртуальную машину в развертывании.</span><span class="sxs-lookup"><span data-stu-id="0972b-117">This command shuts down a virtual machine that the specified service contains and allows deallocation of the last virtual machine in the deployment.</span></span>

### <span data-ttu-id="0972b-118">Пример 5: Отключение нескольких виртуальных машин</span><span class="sxs-lookup"><span data-stu-id="0972b-118">Example 5: Shut down multiple VMs</span></span>
```
PS C:\> Stop-AzureVM -ServiceName "PSTestService" -Name "*" -Force
```

<span data-ttu-id="0972b-119">Эта команда завершает работу нескольких виртуальных машин, которые содержат указанную службу.</span><span class="sxs-lookup"><span data-stu-id="0972b-119">This command shuts down multiple virtual machines that the specified service contains.</span></span>

## <span data-ttu-id="0972b-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0972b-120">PARAMETERS</span></span>

### <span data-ttu-id="0972b-121">-Force</span><span class="sxs-lookup"><span data-stu-id="0972b-121">-Force</span></span>
<span data-ttu-id="0972b-122">Указывает, следует ли разрешить изъятие последней виртуальной машины в развертывании.</span><span class="sxs-lookup"><span data-stu-id="0972b-122">Specifies whether to allow the deallocation of the last virtual machine in a deployment.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0972b-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="0972b-123">-InformationAction</span></span>
<span data-ttu-id="0972b-124">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="0972b-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="0972b-125">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="0972b-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0972b-126">Продолжал</span><span class="sxs-lookup"><span data-stu-id="0972b-126">Continue</span></span>
- <span data-ttu-id="0972b-127">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="0972b-127">Ignore</span></span>
- <span data-ttu-id="0972b-128">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="0972b-128">Inquire</span></span>
- <span data-ttu-id="0972b-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="0972b-129">SilentlyContinue</span></span>
- <span data-ttu-id="0972b-130">Остановить</span><span class="sxs-lookup"><span data-stu-id="0972b-130">Stop</span></span>
- <span data-ttu-id="0972b-131">Рвать</span><span class="sxs-lookup"><span data-stu-id="0972b-131">Suspend</span></span>

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

### <span data-ttu-id="0972b-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="0972b-132">-InformationVariable</span></span>
<span data-ttu-id="0972b-133">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="0972b-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="0972b-134">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0972b-134">-Name</span></span>
<span data-ttu-id="0972b-135">Указывает имя виртуальной машины, которую нужно выключить.</span><span class="sxs-lookup"><span data-stu-id="0972b-135">Specifies the name of the virtual machine to shut down.</span></span>

<span data-ttu-id="0972b-136">Используйте подстановочный знак для асинхронной остановки нескольких виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="0972b-136">Use the wildcard character to stop multiple virtual machines asynchronously.</span></span>
<span data-ttu-id="0972b-137">С подстановочными знаками этот командлет вызывает операцию завершения работы ролей https://msdn.microsoft.com/en-us/library/azure/dn469421.aspx ( https://msdn.microsoft.com/en-us/library/azure/dn469421.aspx) вместо операции завершения работы роли https://msdn.microsoft.com/en-us/library/azure/jj157195.aspx () https://msdn.microsoft.com/en-us/library/azure/jj157195.aspx) .</span><span class="sxs-lookup"><span data-stu-id="0972b-137">With a wildcard character, this cmdlet calls the Shutdown Roleshttps://msdn.microsoft.com/en-us/library/azure/dn469421.aspx operation (https://msdn.microsoft.com/en-us/library/azure/dn469421.aspx), instead of the Shutdown Rolehttps://msdn.microsoft.com/en-us/library/azure/jj157195.aspx operation (https://msdn.microsoft.com/en-us/library/azure/jj157195.aspx).</span></span>

```yaml
Type: String[]
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0972b-138">-Profile</span><span class="sxs-lookup"><span data-stu-id="0972b-138">-Profile</span></span>
<span data-ttu-id="0972b-139">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="0972b-139">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0972b-140">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0972b-140">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0972b-141">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="0972b-141">-ServiceName</span></span>
<span data-ttu-id="0972b-142">Указывает имя службы Azure, которая содержит виртуальную машину, которую нужно завершить.</span><span class="sxs-lookup"><span data-stu-id="0972b-142">Specifies the name of the Azure service that contains the virtual machine to shut down.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0972b-143">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="0972b-143">-StayProvisioned</span></span>
<span data-ttu-id="0972b-144">Указывает на то, что этот командлет обеспечивает сохранение подготовленной виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="0972b-144">Specifies that this cmdlet keeps the virtual machine provisioned.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0972b-145">-VM</span><span class="sxs-lookup"><span data-stu-id="0972b-145">-VM</span></span>
<span data-ttu-id="0972b-146">Указывает объект виртуальной машины, который определяет виртуальную машину для завершения работы.</span><span class="sxs-lookup"><span data-stu-id="0972b-146">Specifies a virtual machine object that identifies the virtual machine to shut down.</span></span>

```yaml
Type: IPersistentVM[]
Parameter Sets: Input
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0972b-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0972b-147">CommonParameters</span></span>
<span data-ttu-id="0972b-148">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0972b-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0972b-149">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0972b-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0972b-150">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0972b-150">INPUTS</span></span>

## <span data-ttu-id="0972b-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0972b-151">OUTPUTS</span></span>

## <span data-ttu-id="0972b-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="0972b-152">NOTES</span></span>

## <span data-ttu-id="0972b-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0972b-153">RELATED LINKS</span></span>

[<span data-ttu-id="0972b-154">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="0972b-154">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="0972b-155">New-AzureVM</span><span class="sxs-lookup"><span data-stu-id="0972b-155">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="0972b-156">Restarts-AzureVM</span><span class="sxs-lookup"><span data-stu-id="0972b-156">Restart-AzureVM</span></span>](./Restart-AzureVM.md)

[<span data-ttu-id="0972b-157">Start-AzureVM</span><span class="sxs-lookup"><span data-stu-id="0972b-157">Start-AzureVM</span></span>](./Start-AzureVM.md)


