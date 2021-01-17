---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: F41953F1-9515-4081-8624-6A1494DA4BB2
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmchefextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMChefExtension.md
ms.openlocfilehash: 02647fc2148069e2c408c979e4b258fd0a641fc0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98402943"
---
# <span data-ttu-id="eb420-101">Get-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="eb420-101">Get-AzVMChefExtension</span></span>

## <span data-ttu-id="eb420-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb420-102">SYNOPSIS</span></span>
<span data-ttu-id="eb420-103">Получает сведения о расширении "Он".</span><span class="sxs-lookup"><span data-stu-id="eb420-103">Gets information about a Chef extension.</span></span>

## <span data-ttu-id="eb420-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="eb420-104">SYNTAX</span></span>

### <span data-ttu-id="eb420-105">Linux</span><span class="sxs-lookup"><span data-stu-id="eb420-105">Linux</span></span>
```
Get-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status] [-Linux]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eb420-106">Windows</span><span class="sxs-lookup"><span data-stu-id="eb420-106">Windows</span></span>
```
Get-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status] [-Windows]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eb420-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eb420-107">DESCRIPTION</span></span>
<span data-ttu-id="eb420-108">Для получения сведений о расширении", установленном на виртуальной машине, с его расширением можно получить сведения о cmdlet **Get-AzVMChefExtension.**</span><span class="sxs-lookup"><span data-stu-id="eb420-108">The **Get-AzVMChefExtension** cmdlet gets information about a Chef extension installed on a virtual machine.</span></span>

## <span data-ttu-id="eb420-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="eb420-109">EXAMPLES</span></span>

### <span data-ttu-id="eb420-110">Пример 1. Просмотр подробных сведений о расширении "Валенка" для виртуальной машины Windows</span><span class="sxs-lookup"><span data-stu-id="eb420-110">Example 1: Get the details of Chef extension for a Windows virtual machine</span></span>
```
PS C:\> Get-AzVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -Windows
```

<span data-ttu-id="eb420-111">Эта команда получает расширение "Данный" на виртуальной машине Windows с именем WindowsVM001, которое принадлежит группе ресурсов ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="eb420-111">This command gets the Chef extension from a Windows virtual machine named WindowsVM001 that belongs to the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="eb420-112">Пример 2. Просмотр подробных сведений о расширении "Валенка" для виртуальной машины Linux</span><span class="sxs-lookup"><span data-stu-id="eb420-112">Example 2: Get the details of Chef extension for a Linux virtual machine</span></span>
```
PS C:\> Get-AzVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -Linux
```

<span data-ttu-id="eb420-113">Эта команда получает расширение", которое входит в группу ресурсов ResourceGroup002 на виртуальной машине Linux с именем LinuxVM001.</span><span class="sxs-lookup"><span data-stu-id="eb420-113">This command gets the Chef extension from a Linux virtual machine named LinuxVM001 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="eb420-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eb420-114">PARAMETERS</span></span>

### <span data-ttu-id="eb420-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb420-115">-DefaultProfile</span></span>
<span data-ttu-id="eb420-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="eb420-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eb420-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="eb420-117">-Linux</span></span>
<span data-ttu-id="eb420-118">Указывает на то, что этот cmdlet работает на виртуальной машине Linux.</span><span class="sxs-lookup"><span data-stu-id="eb420-118">Indicates that this cmdlet works on a Linux virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb420-119">-Name</span><span class="sxs-lookup"><span data-stu-id="eb420-119">-Name</span></span>
<span data-ttu-id="eb420-120">Указывает имя расширения "Валенка".</span><span class="sxs-lookup"><span data-stu-id="eb420-120">Specifies the name of the Chef extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb420-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb420-121">-ResourceGroupName</span></span>
<span data-ttu-id="eb420-122">Имя группы ресурсов, которая содержит виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="eb420-122">Specifies the name of the resource group that contains the virtual machine.</span></span>

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

### <span data-ttu-id="eb420-123">-Status</span><span class="sxs-lookup"><span data-stu-id="eb420-123">-Status</span></span>
<span data-ttu-id="eb420-124">Указывает на то, что этот cmdlet получает только представление экземпляра расширения "Валенка".</span><span class="sxs-lookup"><span data-stu-id="eb420-124">Indicates that this cmdlet gets only the instance view of the Chef extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb420-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="eb420-125">-VMName</span></span>
<span data-ttu-id="eb420-126">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="eb420-126">Specifies the name of a virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb420-127">-Windows</span><span class="sxs-lookup"><span data-stu-id="eb420-127">-Windows</span></span>
<span data-ttu-id="eb420-128">Указывает на то, что этот cmdlet для виртуальной машины Windows.</span><span class="sxs-lookup"><span data-stu-id="eb420-128">Indicates that this cmdlet is for a Windows virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb420-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb420-129">CommonParameters</span></span>
<span data-ttu-id="eb420-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb420-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb420-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eb420-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb420-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="eb420-132">INPUTS</span></span>

### <span data-ttu-id="eb420-133">System.String</span><span class="sxs-lookup"><span data-stu-id="eb420-133">System.String</span></span>

### <span data-ttu-id="eb420-134">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="eb420-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="eb420-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="eb420-135">OUTPUTS</span></span>

### <span data-ttu-id="eb420-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMa modelseExtension</span><span class="sxs-lookup"><span data-stu-id="eb420-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="eb420-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="eb420-137">NOTES</span></span>

## <span data-ttu-id="eb420-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eb420-138">RELATED LINKS</span></span>

[<span data-ttu-id="eb420-139">Set-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="eb420-139">Set-AzVMChefExtension</span></span>](./Set-AzVMChefExtension.md)

[<span data-ttu-id="eb420-140">Remove-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="eb420-140">Remove-AzVMChefExtension</span></span>](./Remove-AzVMChefExtension.md)


