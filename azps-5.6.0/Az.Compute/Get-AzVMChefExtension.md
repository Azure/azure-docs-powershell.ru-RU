---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: F41953F1-9515-4081-8624-6A1494DA4BB2
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmchefextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMChefExtension.md
ms.openlocfilehash: c0d672636d273bcd6e1d2c5f3ebc1c3b70a7b208
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013859"
---
# <span data-ttu-id="53a77-101">Get-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="53a77-101">Get-AzVMChefExtension</span></span>

## <span data-ttu-id="53a77-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53a77-102">SYNOPSIS</span></span>
<span data-ttu-id="53a77-103">Получает сведения о расширении "Сетя".</span><span class="sxs-lookup"><span data-stu-id="53a77-103">Gets information about a Chef extension.</span></span>

## <span data-ttu-id="53a77-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="53a77-104">SYNTAX</span></span>

### <span data-ttu-id="53a77-105">Linux</span><span class="sxs-lookup"><span data-stu-id="53a77-105">Linux</span></span>
```
Get-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status] [-Linux]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53a77-106">Windows</span><span class="sxs-lookup"><span data-stu-id="53a77-106">Windows</span></span>
```
Get-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status] [-Windows]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="53a77-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="53a77-107">DESCRIPTION</span></span>
<span data-ttu-id="53a77-108">Для получения сведений о расширении", установленном на виртуальной машине, можно получить сведения о расширении Для **AzVMChefExtension.**</span><span class="sxs-lookup"><span data-stu-id="53a77-108">The **Get-AzVMChefExtension** cmdlet gets information about a Chef extension installed on a virtual machine.</span></span>

## <span data-ttu-id="53a77-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="53a77-109">EXAMPLES</span></span>

### <span data-ttu-id="53a77-110">Пример 1. Просмотр подробных сведений о расширении "Валенка" для виртуальной машины Windows</span><span class="sxs-lookup"><span data-stu-id="53a77-110">Example 1: Get the details of Chef extension for a Windows virtual machine</span></span>
```
PS C:\> Get-AzVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -Windows
```

<span data-ttu-id="53a77-111">Эта команда получает расширение "Данный" на виртуальной машине Windows с именем WindowsVM001, которое принадлежит к группе ресурсов ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="53a77-111">This command gets the Chef extension from a Windows virtual machine named WindowsVM001 that belongs to the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="53a77-112">Пример 2. Просмотр подробных сведений о расширении "Валенка" для виртуальной машины Linux</span><span class="sxs-lookup"><span data-stu-id="53a77-112">Example 2: Get the details of Chef extension for a Linux virtual machine</span></span>
```
PS C:\> Get-AzVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -Linux
```

<span data-ttu-id="53a77-113">Эта команда получает расширение", которое входит в группу ресурсов ResourceGroup002, с виртуальной машины Linux Linux с именем LinuxVM001.</span><span class="sxs-lookup"><span data-stu-id="53a77-113">This command gets the Chef extension from a Linux virtual machine named LinuxVM001 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="53a77-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="53a77-114">PARAMETERS</span></span>

### <span data-ttu-id="53a77-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53a77-115">-DefaultProfile</span></span>
<span data-ttu-id="53a77-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="53a77-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53a77-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="53a77-117">-Linux</span></span>
<span data-ttu-id="53a77-118">Указывает на то, что этот cmdlet работает на виртуальной машине Linux.</span><span class="sxs-lookup"><span data-stu-id="53a77-118">Indicates that this cmdlet works on a Linux virtual machine.</span></span>

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

### <span data-ttu-id="53a77-119">-Name</span><span class="sxs-lookup"><span data-stu-id="53a77-119">-Name</span></span>
<span data-ttu-id="53a77-120">Указывает имя расширения "Валенка".</span><span class="sxs-lookup"><span data-stu-id="53a77-120">Specifies the name of the Chef extension.</span></span>

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

### <span data-ttu-id="53a77-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53a77-121">-ResourceGroupName</span></span>
<span data-ttu-id="53a77-122">Имя группы ресурсов, которая содержит виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="53a77-122">Specifies the name of the resource group that contains the virtual machine.</span></span>

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

### <span data-ttu-id="53a77-123">-Status</span><span class="sxs-lookup"><span data-stu-id="53a77-123">-Status</span></span>
<span data-ttu-id="53a77-124">Указывает на то, что этот cmdlet получает только представление экземпляра расширения "Валенка".</span><span class="sxs-lookup"><span data-stu-id="53a77-124">Indicates that this cmdlet gets only the instance view of the Chef extension.</span></span>

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

### <span data-ttu-id="53a77-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="53a77-125">-VMName</span></span>
<span data-ttu-id="53a77-126">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="53a77-126">Specifies the name of a virtual machine.</span></span>

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

### <span data-ttu-id="53a77-127">-Windows</span><span class="sxs-lookup"><span data-stu-id="53a77-127">-Windows</span></span>
<span data-ttu-id="53a77-128">Указывает на то, что этот cmdlet для виртуальной машины Windows.</span><span class="sxs-lookup"><span data-stu-id="53a77-128">Indicates that this cmdlet is for a Windows virtual machine.</span></span>

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

### <span data-ttu-id="53a77-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53a77-129">CommonParameters</span></span>
<span data-ttu-id="53a77-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53a77-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53a77-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="53a77-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53a77-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="53a77-132">INPUTS</span></span>

### <span data-ttu-id="53a77-133">System.String</span><span class="sxs-lookup"><span data-stu-id="53a77-133">System.String</span></span>

### <span data-ttu-id="53a77-134">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="53a77-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="53a77-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="53a77-135">OUTPUTS</span></span>

### <span data-ttu-id="53a77-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMa modelseExtension</span><span class="sxs-lookup"><span data-stu-id="53a77-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="53a77-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="53a77-137">NOTES</span></span>

## <span data-ttu-id="53a77-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="53a77-138">RELATED LINKS</span></span>

[<span data-ttu-id="53a77-139">Set-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="53a77-139">Set-AzVMChefExtension</span></span>](./Set-AzVMChefExtension.md)

[<span data-ttu-id="53a77-140">Remove-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="53a77-140">Remove-AzVMChefExtension</span></span>](./Remove-AzVMChefExtension.md)


