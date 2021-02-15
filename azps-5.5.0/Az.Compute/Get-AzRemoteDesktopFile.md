---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: E2A56E55-30A3-4A2F-80AE-9D166840909E
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azremotedesktopfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzRemoteDesktopFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzRemoteDesktopFile.md
ms.openlocfilehash: 650602ef229dd6c7371c6befebbb15dacae1d706
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238896"
---
# <span data-ttu-id="ec00b-101">Get-AzRemoteDesktopFile</span><span class="sxs-lookup"><span data-stu-id="ec00b-101">Get-AzRemoteDesktopFile</span></span>

## <span data-ttu-id="ec00b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec00b-102">SYNOPSIS</span></span>
<span data-ttu-id="ec00b-103">Возвращает RDP-файл.</span><span class="sxs-lookup"><span data-stu-id="ec00b-103">Gets an .rdp file.</span></span>

## <span data-ttu-id="ec00b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ec00b-104">SYNTAX</span></span>

### <span data-ttu-id="ec00b-105">Скачать</span><span class="sxs-lookup"><span data-stu-id="ec00b-105">Download</span></span>
```
Get-AzRemoteDesktopFile [-ResourceGroupName] <String> [-Name] <String> [-LocalPath] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ec00b-106">Запуск</span><span class="sxs-lookup"><span data-stu-id="ec00b-106">Launch</span></span>
```
Get-AzRemoteDesktopFile [-ResourceGroupName] <String> [-Name] <String> [[-LocalPath] <String>] [-Launch]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec00b-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ec00b-107">DESCRIPTION</span></span>
<span data-ttu-id="ec00b-108">Для **этого с помощью cmdlet Get-AzRemoteDesktopFile** будет удален RDP-файл.</span><span class="sxs-lookup"><span data-stu-id="ec00b-108">The **Get-AzRemoteDesktopFile** cmdlet gets a Remote Desktop Protocol (.rdp) file.</span></span>

## <span data-ttu-id="ec00b-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ec00b-109">EXAMPLES</span></span>

### <span data-ttu-id="ec00b-110">Пример 1. Получить файл удаленного рабочего стола</span><span class="sxs-lookup"><span data-stu-id="ec00b-110">Example 1: Get a Remote Desktop file</span></span>
```
PS C:\> Get-AzRemoteDesktopFile -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -LocalPath "D:\RemoteDesktopFile07.rdp"
```

<span data-ttu-id="ec00b-111">Эта команда получает файл удаленного рабочего стола для виртуальной машины с именем VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="ec00b-111">This command gets the Remote Desktop file for the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="ec00b-112">Команда сохраняет результат в файле D:\RemoteDesktopFile07.rdp.</span><span class="sxs-lookup"><span data-stu-id="ec00b-112">The command stores the result in the file named D:\RemoteDesktopFile07.rdp.</span></span>

## <span data-ttu-id="ec00b-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ec00b-113">PARAMETERS</span></span>

### <span data-ttu-id="ec00b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec00b-114">-DefaultProfile</span></span>
<span data-ttu-id="ec00b-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ec00b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec00b-116">-Launch</span><span class="sxs-lookup"><span data-stu-id="ec00b-116">-Launch</span></span>
<span data-ttu-id="ec00b-117">Означает, что этот cmdlet запускает удаленный рабочий стол после того, как он получает RDP-файл.</span><span class="sxs-lookup"><span data-stu-id="ec00b-117">Indicates that this cmdlet launches Remote Desktop after it gets the .rdp file.</span></span>

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

### <span data-ttu-id="ec00b-118">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="ec00b-118">-LocalPath</span></span>
<span data-ttu-id="ec00b-119">Указывает локальный полный путь, в котором этот cmdlet хранит RDP-файл.</span><span class="sxs-lookup"><span data-stu-id="ec00b-119">Specifies the local full path where this cmdlet stores the .rdp file.</span></span>

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

### <span data-ttu-id="ec00b-120">-Name</span><span class="sxs-lookup"><span data-stu-id="ec00b-120">-Name</span></span>
<span data-ttu-id="ec00b-121">Определяет имя набора доступности, который получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ec00b-121">Specifies the name of the availability set that this cmdlet gets.</span></span>

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

### <span data-ttu-id="ec00b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec00b-122">-ResourceGroupName</span></span>
<span data-ttu-id="ec00b-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ec00b-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="ec00b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec00b-124">CommonParameters</span></span>
<span data-ttu-id="ec00b-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec00b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec00b-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ec00b-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec00b-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ec00b-127">INPUTS</span></span>

### <span data-ttu-id="ec00b-128">System.String</span><span class="sxs-lookup"><span data-stu-id="ec00b-128">System.String</span></span>

## <span data-ttu-id="ec00b-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ec00b-129">OUTPUTS</span></span>

### <span data-ttu-id="ec00b-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="ec00b-130">System.Void</span></span>

## <span data-ttu-id="ec00b-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ec00b-131">NOTES</span></span>

## <span data-ttu-id="ec00b-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ec00b-132">RELATED LINKS</span></span>
