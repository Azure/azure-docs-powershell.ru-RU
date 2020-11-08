---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 8A6B2633-EECC-416A-85F6-69C8341AA970
online version: ''
schema: 2.0.0
ms.openlocfilehash: 82ef50dcdf5f17e044a9dc2091cbfda5cb5d1b2a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075620"
---
# <span data-ttu-id="4afa2-101">Get-AzureRemoteDesktopFile</span><span class="sxs-lookup"><span data-stu-id="4afa2-101">Get-AzureRemoteDesktopFile</span></span>

## <span data-ttu-id="4afa2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4afa2-102">SYNOPSIS</span></span>
<span data-ttu-id="4afa2-103">Получает RDP-файл для виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="4afa2-103">Gets an RDP file for an Azure virtual machine.</span></span>

## <span data-ttu-id="4afa2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4afa2-104">SYNTAX</span></span>

### <span data-ttu-id="4afa2-105">Скачать (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4afa2-105">Download (Default)</span></span>
```
Get-AzureRemoteDesktopFile [-Name] <String> [-LocalPath] <String> [-ServiceName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="4afa2-106">Запускающ</span><span class="sxs-lookup"><span data-stu-id="4afa2-106">Launch</span></span>
```
Get-AzureRemoteDesktopFile [-Name] <String> [[-LocalPath] <String>] [-Launch] [-ServiceName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="4afa2-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4afa2-107">DESCRIPTION</span></span>
<span data-ttu-id="4afa2-108">Командлет **Get-AzureRemoteDesktopFile** загружает и сохраняет файл подключения к удаленному рабочему столу (RDP) для виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="4afa2-108">The **Get-AzureRemoteDesktopFile** cmdlet downloads and saves a remote desktop connection (RDP) file for an Azure virtual machine.</span></span>
<span data-ttu-id="4afa2-109">Командлет может запустить подключение к удаленному рабочему столу для указанной виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="4afa2-109">The cmdlet can launch a remote desktop connection to the specified virtual machine.</span></span>

## <span data-ttu-id="4afa2-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4afa2-110">EXAMPLES</span></span>

### <span data-ttu-id="4afa2-111">Пример 1: получение RDP-файла</span><span class="sxs-lookup"><span data-stu-id="4afa2-111">Example 1: Get an RDP file</span></span>
```
PS C:\> Get-AzureRemoteDesktopFile -ServiceName "ContosoService" -Name "VirtualMachine07" -LocalPath "C:\temp\VirtualMachine07.rdp"
```

<span data-ttu-id="4afa2-112">Эта команда получает RDP-файл для виртуальной машины VirtualMachine07 с именем VirtualMachine07, который выполняется в службе с именем ContosoService.</span><span class="sxs-lookup"><span data-stu-id="4afa2-112">This command gets an RDP file for the VirtualMachine07 virtual machine named VirtualMachine07 that runs on the service named ContosoService.</span></span>
<span data-ttu-id="4afa2-113">Команда хранит этот файл как C:\temp\VirtualMachine07.rdp.</span><span class="sxs-lookup"><span data-stu-id="4afa2-113">The command stores that file as C:\temp\VirtualMachine07.rdp.</span></span>

### <span data-ttu-id="4afa2-114">Пример 2: начало удаленного сеанса</span><span class="sxs-lookup"><span data-stu-id="4afa2-114">Example 2: Start a remote session</span></span>
```
PS C:\> Get-AzureRemoteDesktopFile -ServiceName "ContosoService" -Name "VirtualMachine07" -Launch
```

<span data-ttu-id="4afa2-115">Эта команда получает RDP-файл для виртуальной машины VirtualMachine07 с именем VirtualMachine07, который выполняется в службе с именем ContosoService.</span><span class="sxs-lookup"><span data-stu-id="4afa2-115">This command gets an RDP file for the VirtualMachine07 virtual machine named VirtualMachine07 that runs on the service named ContosoService.</span></span>
<span data-ttu-id="4afa2-116">Команда запускает сеанс подключения к удаленному рабочему столу.</span><span class="sxs-lookup"><span data-stu-id="4afa2-116">The command launches a remote desktop session.</span></span>
<span data-ttu-id="4afa2-117">Команда удаляет RDP-файл при закрытом соединении.</span><span class="sxs-lookup"><span data-stu-id="4afa2-117">The command deletes the RDP file when the connection is closed.</span></span>

## <span data-ttu-id="4afa2-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4afa2-118">PARAMETERS</span></span>

### <span data-ttu-id="4afa2-119">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="4afa2-119">-InformationAction</span></span>
<span data-ttu-id="4afa2-120">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="4afa2-120">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="4afa2-121">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="4afa2-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4afa2-122">Продолжал</span><span class="sxs-lookup"><span data-stu-id="4afa2-122">Continue</span></span>
- <span data-ttu-id="4afa2-123">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="4afa2-123">Ignore</span></span>
- <span data-ttu-id="4afa2-124">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="4afa2-124">Inquire</span></span>
- <span data-ttu-id="4afa2-125">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="4afa2-125">SilentlyContinue</span></span>
- <span data-ttu-id="4afa2-126">Остановить</span><span class="sxs-lookup"><span data-stu-id="4afa2-126">Stop</span></span>
- <span data-ttu-id="4afa2-127">Рвать</span><span class="sxs-lookup"><span data-stu-id="4afa2-127">Suspend</span></span>

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

### <span data-ttu-id="4afa2-128">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="4afa2-128">-InformationVariable</span></span>
<span data-ttu-id="4afa2-129">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="4afa2-129">Specifies an information variable.</span></span>

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

### <span data-ttu-id="4afa2-130">-Launch</span><span class="sxs-lookup"><span data-stu-id="4afa2-130">-Launch</span></span>
<span data-ttu-id="4afa2-131">Указывает на то, что этот командлет запускает сеанс подключения к удаленному рабочему столу для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="4afa2-131">Indicates that this cmdlet starts a remote desktop session to the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Launch
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4afa2-132">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="4afa2-132">-LocalPath</span></span>
<span data-ttu-id="4afa2-133">Указывает полный путь скачанного RDP-файла на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="4afa2-133">Specifies the full path of the downloaded RDP file on the local computer.</span></span>

```yaml
Type: String
Parameter Sets: Download
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Launch
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4afa2-134">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4afa2-134">-Name</span></span>
<span data-ttu-id="4afa2-135">Указывает виртуальную машину, для которой этот командлет загружает RDP-файл.</span><span class="sxs-lookup"><span data-stu-id="4afa2-135">Specifies the virtual machine for which this cmdlet downloads an RDP file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: InstanceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4afa2-136">-Profile</span><span class="sxs-lookup"><span data-stu-id="4afa2-136">-Profile</span></span>
<span data-ttu-id="4afa2-137">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="4afa2-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4afa2-138">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4afa2-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4afa2-139">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="4afa2-139">-ServiceName</span></span>
<span data-ttu-id="4afa2-140">Указывает имя службы Azure, к которой принадлежит виртуальная машина.</span><span class="sxs-lookup"><span data-stu-id="4afa2-140">Specifies the name of the Azure service to which the virtual machine belongs.</span></span>

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

### <span data-ttu-id="4afa2-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4afa2-141">CommonParameters</span></span>
<span data-ttu-id="4afa2-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4afa2-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4afa2-143">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4afa2-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4afa2-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4afa2-144">INPUTS</span></span>

## <span data-ttu-id="4afa2-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4afa2-145">OUTPUTS</span></span>

## <span data-ttu-id="4afa2-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="4afa2-146">NOTES</span></span>

## <span data-ttu-id="4afa2-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4afa2-147">RELATED LINKS</span></span>

