---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 78099E89-63C9-4019-A4ED-EF37D2383A09
online version: ''
schema: 2.0.0
ms.openlocfilehash: 23e6165e50c227320875fa70e97d63b0cdd78781
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075677"
---
# <span data-ttu-id="20fd7-101">Export-AzureVM</span><span class="sxs-lookup"><span data-stu-id="20fd7-101">Export-AzureVM</span></span>

## <span data-ttu-id="20fd7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="20fd7-102">SYNOPSIS</span></span>
<span data-ttu-id="20fd7-103">Экспортирует состояние виртуальной машины Azure в файл.</span><span class="sxs-lookup"><span data-stu-id="20fd7-103">Exports an Azure virtual machine state to a file.</span></span>

## <span data-ttu-id="20fd7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="20fd7-104">SYNTAX</span></span>

```
Export-AzureVM [-ServiceName] <String> [-Name] <String> [-Path] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="20fd7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="20fd7-105">DESCRIPTION</span></span>
<span data-ttu-id="20fd7-106">Командлет **Export-AzureVM** экспортирует состояние виртуальной машины в XML-файл.</span><span class="sxs-lookup"><span data-stu-id="20fd7-106">The **Export-AzureVM** cmdlet exports the state of a virtual machine to an .xml file.</span></span>

<span data-ttu-id="20fd7-107">После выполнения команды **Export-azurevm** и **recreate** -Azurevm, а затем **Import-azurevm** для повторного создания виртуальной машины, может возникнуть причина, по которой результирующая виртуальная машина будет отличаться от первоначального IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="20fd7-107">Running **Export-AzureVM** , followed by **Remove-AzureVM** and then **Import-AzureVM** to recreate a virtual machine can cause the resultant virtual machine to have a different IP address than the original.</span></span>

## <span data-ttu-id="20fd7-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="20fd7-108">EXAMPLES</span></span>

### <span data-ttu-id="20fd7-109">Пример 1: экспорт виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="20fd7-109">Example 1: Export a virtual machine</span></span>
```
PS C:\> Export-AzureVM -ServiceName "ContosoService" -Name "ContosoRole06" -Path "C:\vms\VMstate.xml"
```

<span data-ttu-id="20fd7-110">Эта команда экспортирует состояние указанной виртуальной машины в файл VMstate.xml.</span><span class="sxs-lookup"><span data-stu-id="20fd7-110">This command exports the state of the specified virtual machine to the VMstate.xml file.</span></span>

## <span data-ttu-id="20fd7-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="20fd7-111">PARAMETERS</span></span>

### <span data-ttu-id="20fd7-112">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="20fd7-112">-InformationAction</span></span>
<span data-ttu-id="20fd7-113">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="20fd7-113">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="20fd7-114">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="20fd7-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="20fd7-115">Продолжал</span><span class="sxs-lookup"><span data-stu-id="20fd7-115">Continue</span></span>
- <span data-ttu-id="20fd7-116">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="20fd7-116">Ignore</span></span>
- <span data-ttu-id="20fd7-117">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="20fd7-117">Inquire</span></span>
- <span data-ttu-id="20fd7-118">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="20fd7-118">SilentlyContinue</span></span>
- <span data-ttu-id="20fd7-119">Остановить</span><span class="sxs-lookup"><span data-stu-id="20fd7-119">Stop</span></span>
- <span data-ttu-id="20fd7-120">Рвать</span><span class="sxs-lookup"><span data-stu-id="20fd7-120">Suspend</span></span>

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

### <span data-ttu-id="20fd7-121">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="20fd7-121">-InformationVariable</span></span>
<span data-ttu-id="20fd7-122">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="20fd7-122">Specifies an information variable.</span></span>

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

### <span data-ttu-id="20fd7-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="20fd7-123">-Name</span></span>
<span data-ttu-id="20fd7-124">Указывает имя виртуальной машины, для которой этот командлет экспортирует состояние.</span><span class="sxs-lookup"><span data-stu-id="20fd7-124">Specifies the name of the virtual machine for which this cmdlet exports state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20fd7-125">-Path</span><span class="sxs-lookup"><span data-stu-id="20fd7-125">-Path</span></span>
<span data-ttu-id="20fd7-126">Указывает путь и имя файла, в который этот командлет сохраняет состояние виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="20fd7-126">Specifies the path and file name to which this cmdlet saves the virtual machine state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20fd7-127">-Profile</span><span class="sxs-lookup"><span data-stu-id="20fd7-127">-Profile</span></span>
<span data-ttu-id="20fd7-128">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="20fd7-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="20fd7-129">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="20fd7-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="20fd7-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="20fd7-130">-ServiceName</span></span>
<span data-ttu-id="20fd7-131">Указывает имя службы Azure, на которой размещена виртуальная машина.</span><span class="sxs-lookup"><span data-stu-id="20fd7-131">Specifies the name of the Azure service that hosts the virtual machine.</span></span>

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

### <span data-ttu-id="20fd7-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20fd7-132">CommonParameters</span></span>
<span data-ttu-id="20fd7-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="20fd7-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20fd7-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20fd7-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20fd7-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="20fd7-135">INPUTS</span></span>

## <span data-ttu-id="20fd7-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="20fd7-136">OUTPUTS</span></span>

## <span data-ttu-id="20fd7-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="20fd7-137">NOTES</span></span>

## <span data-ttu-id="20fd7-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="20fd7-138">RELATED LINKS</span></span>

[<span data-ttu-id="20fd7-139">Import-AzureVM</span><span class="sxs-lookup"><span data-stu-id="20fd7-139">Import-AzureVM</span></span>](./Import-AzureVM.md)


