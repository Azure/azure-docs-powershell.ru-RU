---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: E2A56E55-30A3-4A2F-80AE-9D166840909E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermremotedesktopfile
schema: 2.0.0
ms.openlocfilehash: e8b19272ed7b6c68221e34cef0395f0592b3013d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913689"
---
# <span data-ttu-id="f2667-101">Get-AzureRmRemoteDesktopFile</span><span class="sxs-lookup"><span data-stu-id="f2667-101">Get-AzureRmRemoteDesktopFile</span></span>

## <span data-ttu-id="f2667-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f2667-102">SYNOPSIS</span></span>
<span data-ttu-id="f2667-103">Получает RDP-файл.</span><span class="sxs-lookup"><span data-stu-id="f2667-103">Gets an .rdp file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2667-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f2667-104">SYNTAX</span></span>

### <span data-ttu-id="f2667-105">Загрузки</span><span class="sxs-lookup"><span data-stu-id="f2667-105">Download</span></span>
```
Get-AzureRmRemoteDesktopFile [-ResourceGroupName] <String> [-Name] <String> [-LocalPath] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f2667-106">Запускающ</span><span class="sxs-lookup"><span data-stu-id="f2667-106">Launch</span></span>
```
Get-AzureRmRemoteDesktopFile [-ResourceGroupName] <String> [-Name] <String> [[-LocalPath] <String>] [-Launch]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2667-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f2667-107">DESCRIPTION</span></span>
<span data-ttu-id="f2667-108">Командлет **Get-AzureRmRemoteDesktopFile** получает файл протокола удаленного рабочего стола (RDP).</span><span class="sxs-lookup"><span data-stu-id="f2667-108">The **Get-AzureRmRemoteDesktopFile** cmdlet gets a Remote Desktop Protocol (.rdp) file.</span></span>

## <span data-ttu-id="f2667-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f2667-109">EXAMPLES</span></span>

### <span data-ttu-id="f2667-110">Пример 1: получение файла удаленного рабочего стола</span><span class="sxs-lookup"><span data-stu-id="f2667-110">Example 1: Get a Remote Desktop file</span></span>
```
PS C:\> Get-AzureRmRemoteDesktopFile -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -LocalPath "D:\RemoteDesktopFile07.rdp"
```

<span data-ttu-id="f2667-111">Эта команда получает файл удаленного рабочего стола для виртуальной машины с именем VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="f2667-111">This command gets the Remote Desktop file for the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="f2667-112">Команда сохраняет результат в файле с именем D:\RemoteDesktopFile07.rdp.</span><span class="sxs-lookup"><span data-stu-id="f2667-112">The command stores the result in the file named D:\RemoteDesktopFile07.rdp.</span></span>

## <span data-ttu-id="f2667-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f2667-113">PARAMETERS</span></span>

### <span data-ttu-id="f2667-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2667-114">-DefaultProfile</span></span>
<span data-ttu-id="f2667-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f2667-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2667-116">-Launch</span><span class="sxs-lookup"><span data-stu-id="f2667-116">-Launch</span></span>
<span data-ttu-id="f2667-117">Указывает на то, что этот командлет запускает удаленный рабочий стол после того, как он получает RDP-файл.</span><span class="sxs-lookup"><span data-stu-id="f2667-117">Indicates that this cmdlet launches Remote Desktop after it gets the .rdp file.</span></span>

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

### <span data-ttu-id="f2667-118">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="f2667-118">-LocalPath</span></span>
<span data-ttu-id="f2667-119">Указывает локальный полный путь, по которому этот командлет хранит RDP-файл.</span><span class="sxs-lookup"><span data-stu-id="f2667-119">Specifies the local full path where this cmdlet stores the .rdp file.</span></span>

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

### <span data-ttu-id="f2667-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f2667-120">-Name</span></span>
<span data-ttu-id="f2667-121">Указывает имя набора доступности, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="f2667-121">Specifies the name of the availability set that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f2667-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2667-122">-ResourceGroupName</span></span>
<span data-ttu-id="f2667-123">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f2667-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="f2667-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2667-124">CommonParameters</span></span>
<span data-ttu-id="f2667-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f2667-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2667-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2667-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2667-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f2667-127">INPUTS</span></span>

### <span data-ttu-id="f2667-128">Ничего</span><span class="sxs-lookup"><span data-stu-id="f2667-128">None</span></span>
<span data-ttu-id="f2667-129">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="f2667-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f2667-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f2667-130">OUTPUTS</span></span>

## <span data-ttu-id="f2667-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="f2667-131">NOTES</span></span>

## <span data-ttu-id="f2667-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f2667-132">RELATED LINKS</span></span>

