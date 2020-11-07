---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: E2A56E55-30A3-4A2F-80AE-9D166840909E
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azremotedesktopfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzRemoteDesktopFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzRemoteDesktopFile.md
ms.openlocfilehash: 413977ee42b0edc2221cbbdcfd34b6130d40f74e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911550"
---
# <span data-ttu-id="9d199-101">Get-AzRemoteDesktopFile</span><span class="sxs-lookup"><span data-stu-id="9d199-101">Get-AzRemoteDesktopFile</span></span>

## <span data-ttu-id="9d199-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9d199-102">SYNOPSIS</span></span>
<span data-ttu-id="9d199-103">Получает RDP-файл.</span><span class="sxs-lookup"><span data-stu-id="9d199-103">Gets an .rdp file.</span></span>

## <span data-ttu-id="9d199-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9d199-104">SYNTAX</span></span>

### <span data-ttu-id="9d199-105">Загрузки</span><span class="sxs-lookup"><span data-stu-id="9d199-105">Download</span></span>
```
Get-AzRemoteDesktopFile [-ResourceGroupName] <String> [-Name] <String> [-LocalPath] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d199-106">Запускающ</span><span class="sxs-lookup"><span data-stu-id="9d199-106">Launch</span></span>
```
Get-AzRemoteDesktopFile [-ResourceGroupName] <String> [-Name] <String> [[-LocalPath] <String>] [-Launch]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9d199-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9d199-107">DESCRIPTION</span></span>
<span data-ttu-id="9d199-108">Командлет **Get-AzRemoteDesktopFile** получает файл протокола удаленного рабочего стола (RDP).</span><span class="sxs-lookup"><span data-stu-id="9d199-108">The **Get-AzRemoteDesktopFile** cmdlet gets a Remote Desktop Protocol (.rdp) file.</span></span>

## <span data-ttu-id="9d199-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9d199-109">EXAMPLES</span></span>

### <span data-ttu-id="9d199-110">Пример 1: получение файла удаленного рабочего стола</span><span class="sxs-lookup"><span data-stu-id="9d199-110">Example 1: Get a Remote Desktop file</span></span>
```
PS C:\> Get-AzRemoteDesktopFile -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -LocalPath "D:\RemoteDesktopFile07.rdp"
```

<span data-ttu-id="9d199-111">Эта команда получает файл удаленного рабочего стола для виртуальной машины с именем VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="9d199-111">This command gets the Remote Desktop file for the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="9d199-112">Команда сохраняет результат в файле с именем D:\RemoteDesktopFile07.rdp.</span><span class="sxs-lookup"><span data-stu-id="9d199-112">The command stores the result in the file named D:\RemoteDesktopFile07.rdp.</span></span>

## <span data-ttu-id="9d199-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9d199-113">PARAMETERS</span></span>

### <span data-ttu-id="9d199-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d199-114">-DefaultProfile</span></span>
<span data-ttu-id="9d199-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9d199-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d199-116">-Launch</span><span class="sxs-lookup"><span data-stu-id="9d199-116">-Launch</span></span>
<span data-ttu-id="9d199-117">Указывает на то, что этот командлет запускает удаленный рабочий стол после того, как он получает RDP-файл.</span><span class="sxs-lookup"><span data-stu-id="9d199-117">Indicates that this cmdlet launches Remote Desktop after it gets the .rdp file.</span></span>

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

### <span data-ttu-id="9d199-118">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="9d199-118">-LocalPath</span></span>
<span data-ttu-id="9d199-119">Указывает локальный полный путь, по которому этот командлет хранит RDP-файл.</span><span class="sxs-lookup"><span data-stu-id="9d199-119">Specifies the local full path where this cmdlet stores the .rdp file.</span></span>

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

### <span data-ttu-id="9d199-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9d199-120">-Name</span></span>
<span data-ttu-id="9d199-121">Указывает имя набора доступности, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="9d199-121">Specifies the name of the availability set that this cmdlet gets.</span></span>

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

### <span data-ttu-id="9d199-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d199-122">-ResourceGroupName</span></span>
<span data-ttu-id="9d199-123">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9d199-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="9d199-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d199-124">CommonParameters</span></span>
<span data-ttu-id="9d199-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9d199-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d199-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d199-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d199-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9d199-127">INPUTS</span></span>

### <span data-ttu-id="9d199-128">Ничего</span><span class="sxs-lookup"><span data-stu-id="9d199-128">None</span></span>
<span data-ttu-id="9d199-129">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="9d199-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9d199-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9d199-130">OUTPUTS</span></span>

## <span data-ttu-id="9d199-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="9d199-131">NOTES</span></span>

## <span data-ttu-id="9d199-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9d199-132">RELATED LINKS</span></span>

