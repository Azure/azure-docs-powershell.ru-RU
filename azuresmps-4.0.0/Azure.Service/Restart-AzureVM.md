---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 596B8A6F-D3C2-4170-BCD7-B7A1CDB656D8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7ee767e1ba4c5008837e7cef98aafa4017465829
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076073"
---
# <span data-ttu-id="07a70-101">Restart-AzureVM</span><span class="sxs-lookup"><span data-stu-id="07a70-101">Restart-AzureVM</span></span>

## <span data-ttu-id="07a70-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="07a70-102">SYNOPSIS</span></span>
<span data-ttu-id="07a70-103">Перезапуск виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="07a70-103">Restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="07a70-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="07a70-104">SYNTAX</span></span>

### <span data-ttu-id="07a70-105">RestartByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="07a70-105">RestartByName (Default)</span></span>
```
Restart-AzureVM [-Name] <String> [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="07a70-106">RedeployByName</span><span class="sxs-lookup"><span data-stu-id="07a70-106">RedeployByName</span></span>
```
Restart-AzureVM [-Name] <String> [-Redeploy] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="07a70-107">InitiateMaintenanceByName</span><span class="sxs-lookup"><span data-stu-id="07a70-107">InitiateMaintenanceByName</span></span>
```
Restart-AzureVM [-Name] <String> [-InitiateMaintenance] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="07a70-108">RestartInput</span><span class="sxs-lookup"><span data-stu-id="07a70-108">RestartInput</span></span>
```
Restart-AzureVM -VM <PersistentVM> [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="07a70-109">RedeployInput</span><span class="sxs-lookup"><span data-stu-id="07a70-109">RedeployInput</span></span>
```
Restart-AzureVM -VM <PersistentVM> [-Redeploy] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="07a70-110">InitiateMaintenanceInput</span><span class="sxs-lookup"><span data-stu-id="07a70-110">InitiateMaintenanceInput</span></span>
```
Restart-AzureVM -VM <PersistentVM> [-InitiateMaintenance] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="07a70-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="07a70-111">DESCRIPTION</span></span>
<span data-ttu-id="07a70-112">Командлет **restart-AzureVM** запрашивает перезагрузку виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="07a70-112">The **Restart-AzureVM** cmdlet requests a restart of an Azure virtual machine.</span></span>

## <span data-ttu-id="07a70-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="07a70-113">EXAMPLES</span></span>

### <span data-ttu-id="07a70-114">Пример 1: перезапуск виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="07a70-114">Example 1: Restart a virtual machine</span></span>
```
PS C:\> Restart-AzureVM -ServiceName "MyService01" -Name "MyVM"
```

<span data-ttu-id="07a70-115">Эта команда перезапускает виртуальную машину VirtualMachine27, запущенную в службе Azure с именем Service01.</span><span class="sxs-lookup"><span data-stu-id="07a70-115">This command restarts the VirtualMachine27 virtual machine running in the Azure service named Service01.</span></span>

### <span data-ttu-id="07a70-116">Пример 2: перезапуск виртуальной машины с помощью объекта виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="07a70-116">Example 2: Restart a virtual machine by using a virtual machine object</span></span>
```
PS C:\> Get-AzureVM -ServiceName "MyService01" -Name "VirtualMachine27" | Restart-AzureVM
```

<span data-ttu-id="07a70-117">Эта команда извлекает объект виртуальной машины для виртуальной машины с именем MyVM и перезапускает его.</span><span class="sxs-lookup"><span data-stu-id="07a70-117">This command retrieves the virtual machine object for the virtual machine named MyVM and then restarts it.</span></span>

## <span data-ttu-id="07a70-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="07a70-118">PARAMETERS</span></span>

### <span data-ttu-id="07a70-119">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="07a70-119">-InformationAction</span></span>
<span data-ttu-id="07a70-120">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="07a70-120">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="07a70-121">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="07a70-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="07a70-122">Продолжал</span><span class="sxs-lookup"><span data-stu-id="07a70-122">Continue</span></span>
- <span data-ttu-id="07a70-123">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="07a70-123">Ignore</span></span>
- <span data-ttu-id="07a70-124">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="07a70-124">Inquire</span></span>
- <span data-ttu-id="07a70-125">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="07a70-125">SilentlyContinue</span></span>
- <span data-ttu-id="07a70-126">Остановить</span><span class="sxs-lookup"><span data-stu-id="07a70-126">Stop</span></span>
- <span data-ttu-id="07a70-127">Рвать</span><span class="sxs-lookup"><span data-stu-id="07a70-127">Suspend</span></span>

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

### <span data-ttu-id="07a70-128">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="07a70-128">-InformationVariable</span></span>
<span data-ttu-id="07a70-129">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="07a70-129">Specifies an information variable.</span></span>

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

### <span data-ttu-id="07a70-130">-InitiateMaintenance</span><span class="sxs-lookup"><span data-stu-id="07a70-130">-InitiateMaintenance</span></span>
<span data-ttu-id="07a70-131">Запуск обслуживания на виртуальной машине</span><span class="sxs-lookup"><span data-stu-id="07a70-131">Initiate Maintenance on the Virtual Machine</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: InitiateMaintenanceByName, InitiateMaintenanceInput
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07a70-132">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="07a70-132">-Name</span></span>
<span data-ttu-id="07a70-133">Указывает имя виртуальной машины, которую нужно перезапустить.</span><span class="sxs-lookup"><span data-stu-id="07a70-133">Specifies the name of the virtual machine to restart.</span></span>

```yaml
Type: String
Parameter Sets: RestartByName, RedeployByName, InitiateMaintenanceByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07a70-134">-Profile</span><span class="sxs-lookup"><span data-stu-id="07a70-134">-Profile</span></span>
<span data-ttu-id="07a70-135">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="07a70-135">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="07a70-136">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="07a70-136">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="07a70-137">-Повторное развертывание</span><span class="sxs-lookup"><span data-stu-id="07a70-137">-Redeploy</span></span>
<span data-ttu-id="07a70-138">Указывает на повторное развертывание виртуальной машины командлетом.</span><span class="sxs-lookup"><span data-stu-id="07a70-138">Indicates that the cmdlet redeploys the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RedeployByName, RedeployInput
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07a70-139">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="07a70-139">-ServiceName</span></span>
<span data-ttu-id="07a70-140">Указывает имя службы Azure, которая содержит виртуальную машину, которую нужно перезапустить.</span><span class="sxs-lookup"><span data-stu-id="07a70-140">Specifies the name of the Azure service that contains the virtual machine to restart.</span></span>

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

### <span data-ttu-id="07a70-141">-VM</span><span class="sxs-lookup"><span data-stu-id="07a70-141">-VM</span></span>
<span data-ttu-id="07a70-142">Задает объект виртуальной машины, определяющий виртуальную машину, которую нужно перезапустить.</span><span class="sxs-lookup"><span data-stu-id="07a70-142">Specifies a virtual machine object that identifies the virtual machine to restart.</span></span>

```yaml
Type: PersistentVM
Parameter Sets: RestartInput, RedeployInput, InitiateMaintenanceInput
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="07a70-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07a70-143">CommonParameters</span></span>
<span data-ttu-id="07a70-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="07a70-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07a70-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07a70-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07a70-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="07a70-146">INPUTS</span></span>

## <span data-ttu-id="07a70-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="07a70-147">OUTPUTS</span></span>

## <span data-ttu-id="07a70-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="07a70-148">NOTES</span></span>

## <span data-ttu-id="07a70-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="07a70-149">RELATED LINKS</span></span>

[<span data-ttu-id="07a70-150">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="07a70-150">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="07a70-151">Remove-AzureVM</span><span class="sxs-lookup"><span data-stu-id="07a70-151">Remove-AzureVM</span></span>](./Remove-AzureVM.md)

[<span data-ttu-id="07a70-152">Start-AzureVM</span><span class="sxs-lookup"><span data-stu-id="07a70-152">Start-AzureVM</span></span>](./Start-AzureVM.md)

[<span data-ttu-id="07a70-153">Stop-AzureVM</span><span class="sxs-lookup"><span data-stu-id="07a70-153">Stop-AzureVM</span></span>](./Stop-AzureVM.md)

[<span data-ttu-id="07a70-154">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="07a70-154">Update-AzureVM</span></span>](./Update-AzureVM.md)


