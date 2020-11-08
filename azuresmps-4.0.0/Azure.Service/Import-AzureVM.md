---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7180CAC6-BFC1-4A18-A754-83D5F05C5BEF
online version: ''
schema: 2.0.0
ms.openlocfilehash: c62c30558147bccd9cdecc73925b7e1a379d1c5b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076255"
---
# <span data-ttu-id="ad321-101">Import-AzureVM</span><span class="sxs-lookup"><span data-stu-id="ad321-101">Import-AzureVM</span></span>

## <span data-ttu-id="ad321-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ad321-102">SYNOPSIS</span></span>
<span data-ttu-id="ad321-103">Импортирует состояние виртуальной машины Azure из файла.</span><span class="sxs-lookup"><span data-stu-id="ad321-103">Imports an Azure virtual machine state from a file.</span></span>

## <span data-ttu-id="ad321-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ad321-104">SYNTAX</span></span>

```
Import-AzureVM [-Path] <String> [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="ad321-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ad321-105">DESCRIPTION</span></span>
<span data-ttu-id="ad321-106">Командлет **Import-AzureVM** импортирует сохраненное ранее состояние виртуальной машины из XML-файла.</span><span class="sxs-lookup"><span data-stu-id="ad321-106">The **Import-AzureVM** cmdlet imports the previously saved state of a virtual machine from an XML file.</span></span>
<span data-ttu-id="ad321-107">Этот командлет полезен, если вы хотите впоследствии создать виртуальную машину из импортированных данных.</span><span class="sxs-lookup"><span data-stu-id="ad321-107">This cmdlet is useful when you want to subsequently create a virtual machine from the imported data.</span></span>

<span data-ttu-id="ad321-108">После выполнения команды **Export-azurevm** и **recreate** -Azurevm, а затем **Import-azurevm** для повторного создания виртуальной машины, может возникнуть причина, по которой результирующая виртуальная машина будет отличаться от первоначального IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="ad321-108">Running **Export-AzureVM** , followed by **Remove-AzureVM** and then **Import-AzureVM** to recreate a virtual machine can cause the resultant virtual machine to have a different IP address than the original.</span></span>

## <span data-ttu-id="ad321-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ad321-109">EXAMPLES</span></span>

### <span data-ttu-id="ad321-110">Пример 1: импорт состояния виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="ad321-110">Example 1: Import a virtual machine state</span></span>
```
PS C:\> Import-AzureVM -Path "C:\VMstate.xml" | New-AzureVM -ServiceName "ContosoService02"
```

<span data-ttu-id="ad321-111">Эта команда импортирует состояние виртуальной машины из файла VMstate.xml, а затем создает виртуальную машину в указанной облачной службе.</span><span class="sxs-lookup"><span data-stu-id="ad321-111">This command imports the state of a virtual machine from the VMstate.xml file, and then creates a virtual machine in the specified cloud service.</span></span>

## <span data-ttu-id="ad321-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ad321-112">PARAMETERS</span></span>

### <span data-ttu-id="ad321-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="ad321-113">-InformationAction</span></span>
<span data-ttu-id="ad321-114">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="ad321-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="ad321-115">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="ad321-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ad321-116">Продолжал</span><span class="sxs-lookup"><span data-stu-id="ad321-116">Continue</span></span>
- <span data-ttu-id="ad321-117">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="ad321-117">Ignore</span></span>
- <span data-ttu-id="ad321-118">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="ad321-118">Inquire</span></span>
- <span data-ttu-id="ad321-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="ad321-119">SilentlyContinue</span></span>
- <span data-ttu-id="ad321-120">Остановить</span><span class="sxs-lookup"><span data-stu-id="ad321-120">Stop</span></span>
- <span data-ttu-id="ad321-121">Рвать</span><span class="sxs-lookup"><span data-stu-id="ad321-121">Suspend</span></span>

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

### <span data-ttu-id="ad321-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="ad321-122">-InformationVariable</span></span>
<span data-ttu-id="ad321-123">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="ad321-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="ad321-124">-Path</span><span class="sxs-lookup"><span data-stu-id="ad321-124">-Path</span></span>
<span data-ttu-id="ad321-125">Задает путь к файлу с ранее сохраненным состоянием виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ad321-125">Specifies the path of the file with the previously saved virtual machine state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad321-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad321-126">CommonParameters</span></span>
<span data-ttu-id="ad321-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ad321-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad321-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad321-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad321-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ad321-129">INPUTS</span></span>

## <span data-ttu-id="ad321-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ad321-130">OUTPUTS</span></span>

## <span data-ttu-id="ad321-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="ad321-131">NOTES</span></span>

## <span data-ttu-id="ad321-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ad321-132">RELATED LINKS</span></span>

[<span data-ttu-id="ad321-133">Export-AzureVM</span><span class="sxs-lookup"><span data-stu-id="ad321-133">Export-AzureVM</span></span>](./Export-AzureVM.md)

[<span data-ttu-id="ad321-134">New-AzureVM</span><span class="sxs-lookup"><span data-stu-id="ad321-134">New-AzureVM</span></span>](./New-AzureVM.md)


