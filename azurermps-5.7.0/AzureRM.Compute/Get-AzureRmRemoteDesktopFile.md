---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: E2A56E55-30A3-4A2F-80AE-9D166840909E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmRemoteDesktopFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmRemoteDesktopFile.md
ms.openlocfilehash: f4b29849109959a8b06a8d0339c8927b8a840a7a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732757"
---
# <span data-ttu-id="67210-101">Get-AzureRmRemoteDesktopFile</span><span class="sxs-lookup"><span data-stu-id="67210-101">Get-AzureRmRemoteDesktopFile</span></span>

## <span data-ttu-id="67210-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="67210-102">SYNOPSIS</span></span>
<span data-ttu-id="67210-103">Получает RDP-файл.</span><span class="sxs-lookup"><span data-stu-id="67210-103">Gets an .rdp file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="67210-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="67210-104">SYNTAX</span></span>

### <span data-ttu-id="67210-105">Загрузки</span><span class="sxs-lookup"><span data-stu-id="67210-105">Download</span></span>
```
Get-AzureRmRemoteDesktopFile [-ResourceGroupName] <String> [-Name] <String> [-LocalPath] <String>
 [<CommonParameters>]
```

### <span data-ttu-id="67210-106">Запускающ</span><span class="sxs-lookup"><span data-stu-id="67210-106">Launch</span></span>
```
Get-AzureRmRemoteDesktopFile [-ResourceGroupName] <String> [-Name] <String> [[-LocalPath] <String>] [-Launch]
 [<CommonParameters>]
```

## <span data-ttu-id="67210-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="67210-107">DESCRIPTION</span></span>
<span data-ttu-id="67210-108">Командлет **Get-AzureRmRemoteDesktopFile** получает файл протокола удаленного рабочего стола (RDP).</span><span class="sxs-lookup"><span data-stu-id="67210-108">The **Get-AzureRmRemoteDesktopFile** cmdlet gets a Remote Desktop Protocol (.rdp) file.</span></span>

## <span data-ttu-id="67210-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="67210-109">EXAMPLES</span></span>

### <span data-ttu-id="67210-110">Пример 1: получение файла удаленного рабочего стола</span><span class="sxs-lookup"><span data-stu-id="67210-110">Example 1: Get a Remote Desktop file</span></span>
```
PS C:\> Get-AzureRmRemoteDesktopFile -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -LocalPath "D:\RemoteDesktopFile07.rdp"
```

<span data-ttu-id="67210-111">Эта команда получает файл удаленного рабочего стола для виртуальной машины с именем VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="67210-111">This command gets the Remote Desktop file for the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="67210-112">Команда сохраняет результат в файле с именем D:\RemoteDesktopFile07.rdp.</span><span class="sxs-lookup"><span data-stu-id="67210-112">The command stores the result in the file named D:\RemoteDesktopFile07.rdp.</span></span>

## <span data-ttu-id="67210-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="67210-113">PARAMETERS</span></span>

### <span data-ttu-id="67210-114">-Launch</span><span class="sxs-lookup"><span data-stu-id="67210-114">-Launch</span></span>
<span data-ttu-id="67210-115">Указывает на то, что этот командлет запускает удаленный рабочий стол после того, как он получает RDP-файл.</span><span class="sxs-lookup"><span data-stu-id="67210-115">Indicates that this cmdlet launches Remote Desktop after it gets the .rdp file.</span></span>

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

### <span data-ttu-id="67210-116">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="67210-116">-LocalPath</span></span>
<span data-ttu-id="67210-117">Указывает локальный полный путь, по которому этот командлет хранит RDP-файл.</span><span class="sxs-lookup"><span data-stu-id="67210-117">Specifies the local full path where this cmdlet stores the .rdp file.</span></span>

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

### <span data-ttu-id="67210-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="67210-118">-Name</span></span>
<span data-ttu-id="67210-119">Указывает имя набора доступности, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="67210-119">Specifies the name of the availability set that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67210-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67210-120">-ResourceGroupName</span></span>
<span data-ttu-id="67210-121">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="67210-121">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="67210-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67210-122">CommonParameters</span></span>
<span data-ttu-id="67210-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="67210-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67210-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67210-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67210-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="67210-125">INPUTS</span></span>

### <span data-ttu-id="67210-126">Ничего</span><span class="sxs-lookup"><span data-stu-id="67210-126">None</span></span>
<span data-ttu-id="67210-127">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="67210-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="67210-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="67210-128">OUTPUTS</span></span>

## <span data-ttu-id="67210-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="67210-129">NOTES</span></span>

## <span data-ttu-id="67210-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="67210-130">RELATED LINKS</span></span>

