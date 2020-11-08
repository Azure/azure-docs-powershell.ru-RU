---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: FAB5E55D-95FC-4545-8BA6-EEFCFDB04200
online version: ''
schema: 2.0.0
ms.openlocfilehash: c311653b92219eb3bee0e3b1f8c8fe5caaee9846
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075637"
---
# <span data-ttu-id="faac8-101">Get-AzureOSVersion</span><span class="sxs-lookup"><span data-stu-id="faac8-101">Get-AzureOSVersion</span></span>

## <span data-ttu-id="faac8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="faac8-102">SYNOPSIS</span></span>
<span data-ttu-id="faac8-103">Список всех гостевых операционных систем Azure.</span><span class="sxs-lookup"><span data-stu-id="faac8-103">Lists all Azure guest operating systems.</span></span>

## <span data-ttu-id="faac8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="faac8-104">SYNTAX</span></span>

```
Get-AzureOSVersion [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="faac8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="faac8-105">DESCRIPTION</span></span>
<span data-ttu-id="faac8-106">Командлет **Get-AzureOSVersion** перечисляет все доступные гостевые операционные системы Azure.</span><span class="sxs-lookup"><span data-stu-id="faac8-106">The **Get-AzureOSVersion** cmdlet lists all the available Azure guest operating systems.</span></span>

## <span data-ttu-id="faac8-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="faac8-107">EXAMPLES</span></span>

### <span data-ttu-id="faac8-108">Пример 1: получение всех доступных операционных систем</span><span class="sxs-lookup"><span data-stu-id="faac8-108">Example 1: Get all available operating systems</span></span>
```
PS C:\> Get-AzureOSVersion
```

<span data-ttu-id="faac8-109">Эта команда извлекает объект, содержащий список всех версий гостевых операционных систем, которые доступны в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="faac8-109">This command retrieves an object that contains a list of all versions of guest operating systems that are available in the current subscription.</span></span>

### <span data-ttu-id="faac8-110">Пример 2: отображение сведений об операционной системе в таблице</span><span class="sxs-lookup"><span data-stu-id="faac8-110">Example 2: Display operating system information in a table</span></span>
```
PS C:\> Get-AzureOSVersion | Format-Table -AutoSize -Property "Family", "FamilyLabel", "Version"
```

<span data-ttu-id="faac8-111">Эта команда извлекает объект, содержащий список всех версий гостевых операционных систем, которые доступны в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="faac8-111">This command retrieves an object that contains a list of all versions of guest operating systems that are available in the current subscription.</span></span>
<span data-ttu-id="faac8-112">Команда передает их в командлет **Format-Table** с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="faac8-112">The command passes them to the **Format-Table** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="faac8-113">Этот командлет форматирует их в виде таблицы, в которой указано семейство операционной системы, название семейства операционной системы и версия.</span><span class="sxs-lookup"><span data-stu-id="faac8-113">That cmdlet formats them as a table that shows the operating system family, operating system family label, and version.</span></span>

## <span data-ttu-id="faac8-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="faac8-114">PARAMETERS</span></span>

### <span data-ttu-id="faac8-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="faac8-115">-InformationAction</span></span>
<span data-ttu-id="faac8-116">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="faac8-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="faac8-117">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="faac8-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="faac8-118">Продолжал</span><span class="sxs-lookup"><span data-stu-id="faac8-118">Continue</span></span>
- <span data-ttu-id="faac8-119">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="faac8-119">Ignore</span></span>
- <span data-ttu-id="faac8-120">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="faac8-120">Inquire</span></span>
- <span data-ttu-id="faac8-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="faac8-121">SilentlyContinue</span></span>
- <span data-ttu-id="faac8-122">Остановить</span><span class="sxs-lookup"><span data-stu-id="faac8-122">Stop</span></span>
- <span data-ttu-id="faac8-123">Рвать</span><span class="sxs-lookup"><span data-stu-id="faac8-123">Suspend</span></span>

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

### <span data-ttu-id="faac8-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="faac8-124">-InformationVariable</span></span>
<span data-ttu-id="faac8-125">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="faac8-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="faac8-126">-Profile</span><span class="sxs-lookup"><span data-stu-id="faac8-126">-Profile</span></span>
<span data-ttu-id="faac8-127">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="faac8-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="faac8-128">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="faac8-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="faac8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="faac8-129">CommonParameters</span></span>
<span data-ttu-id="faac8-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="faac8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="faac8-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="faac8-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="faac8-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="faac8-132">INPUTS</span></span>

## <span data-ttu-id="faac8-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="faac8-133">OUTPUTS</span></span>

## <span data-ttu-id="faac8-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="faac8-134">NOTES</span></span>

## <span data-ttu-id="faac8-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="faac8-135">RELATED LINKS</span></span>

[<span data-ttu-id="faac8-136">Get-AzureOSDisk</span><span class="sxs-lookup"><span data-stu-id="faac8-136">Get-AzureOSDisk</span></span>](./Get-AzureOSDisk.md)


