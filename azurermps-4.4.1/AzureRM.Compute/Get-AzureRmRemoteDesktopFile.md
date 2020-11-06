---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: E2A56E55-30A3-4A2F-80AE-9D166840909E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmRemoteDesktopFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmRemoteDesktopFile.md
ms.openlocfilehash: 9e546815c7333bf468a204c6a22f9426c24b65d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560491"
---
# <span data-ttu-id="7c3d9-101">Get-AzureRmRemoteDesktopFile</span><span class="sxs-lookup"><span data-stu-id="7c3d9-101">Get-AzureRmRemoteDesktopFile</span></span>

## <span data-ttu-id="7c3d9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7c3d9-102">SYNOPSIS</span></span>
<span data-ttu-id="7c3d9-103">Получает RDP-файл.</span><span class="sxs-lookup"><span data-stu-id="7c3d9-103">Gets an .rdp file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7c3d9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7c3d9-104">SYNTAX</span></span>

### <span data-ttu-id="7c3d9-105">Загрузки</span><span class="sxs-lookup"><span data-stu-id="7c3d9-105">Download</span></span>
```
Get-AzureRmRemoteDesktopFile [-ResourceGroupName] <String> [-Name] <String> [-LocalPath] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7c3d9-106">Запускающ</span><span class="sxs-lookup"><span data-stu-id="7c3d9-106">Launch</span></span>
```
Get-AzureRmRemoteDesktopFile [-ResourceGroupName] <String> [-Name] <String> [[-LocalPath] <String>] [-Launch]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7c3d9-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7c3d9-107">DESCRIPTION</span></span>
<span data-ttu-id="7c3d9-108">Командлет **Get-AzureRmRemoteDesktopFile** получает файл протокола удаленного рабочего стола (RDP).</span><span class="sxs-lookup"><span data-stu-id="7c3d9-108">The **Get-AzureRmRemoteDesktopFile** cmdlet gets a Remote Desktop Protocol (.rdp) file.</span></span>

## <span data-ttu-id="7c3d9-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7c3d9-109">EXAMPLES</span></span>

### <span data-ttu-id="7c3d9-110">Пример 1: получение файла удаленного рабочего стола</span><span class="sxs-lookup"><span data-stu-id="7c3d9-110">Example 1: Get a Remote Desktop file</span></span>
```
PS C:\> Get-AzureRmRemoteDesktopFile -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -LocalPath "D:\RemoteDesktopFile07.rdp"
```

<span data-ttu-id="7c3d9-111">Эта команда получает файл удаленного рабочего стола для виртуальной машины с именем VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="7c3d9-111">This command gets the Remote Desktop file for the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="7c3d9-112">Команда сохраняет результат в файле с именем D:\RemoteDesktopFile07.rdp.</span><span class="sxs-lookup"><span data-stu-id="7c3d9-112">The command stores the result in the file named D:\RemoteDesktopFile07.rdp.</span></span>

## <span data-ttu-id="7c3d9-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7c3d9-113">PARAMETERS</span></span>

### <span data-ttu-id="7c3d9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c3d9-114">-DefaultProfile</span></span>
<span data-ttu-id="7c3d9-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7c3d9-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c3d9-116">-Launch</span><span class="sxs-lookup"><span data-stu-id="7c3d9-116">-Launch</span></span>
<span data-ttu-id="7c3d9-117">Указывает на то, что этот командлет запускает удаленный рабочий стол после того, как он получает RDP-файл.</span><span class="sxs-lookup"><span data-stu-id="7c3d9-117">Indicates that this cmdlet launches Remote Desktop after it gets the .rdp file.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Launch
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c3d9-118">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="7c3d9-118">-LocalPath</span></span>
<span data-ttu-id="7c3d9-119">Указывает локальный полный путь, по которому этот командлет хранит RDP-файл.</span><span class="sxs-lookup"><span data-stu-id="7c3d9-119">Specifies the local full path where this cmdlet stores the .rdp file.</span></span>

```yaml
Type: System.String
Parameter Sets: Download
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Launch
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c3d9-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7c3d9-120">-Name</span></span>
<span data-ttu-id="7c3d9-121">Указывает имя набора доступности, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="7c3d9-121">Specifies the name of the availability set that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c3d9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c3d9-122">-ResourceGroupName</span></span>
<span data-ttu-id="7c3d9-123">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7c3d9-123">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c3d9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c3d9-124">CommonParameters</span></span>
<span data-ttu-id="7c3d9-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7c3d9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c3d9-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c3d9-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c3d9-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7c3d9-127">INPUTS</span></span>

## <span data-ttu-id="7c3d9-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7c3d9-128">OUTPUTS</span></span>

## <span data-ttu-id="7c3d9-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="7c3d9-129">NOTES</span></span>

## <span data-ttu-id="7c3d9-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7c3d9-130">RELATED LINKS</span></span>

