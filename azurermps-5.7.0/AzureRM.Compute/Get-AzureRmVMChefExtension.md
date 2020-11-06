---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: F41953F1-9515-4081-8624-6A1494DA4BB2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMChefExtension.md
ms.openlocfilehash: 5733939c24437c974f629588106d6240766a9df1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563708"
---
# <span data-ttu-id="db213-101">Get-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="db213-101">Get-AzureRmVMChefExtension</span></span>

## <span data-ttu-id="db213-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="db213-102">SYNOPSIS</span></span>
<span data-ttu-id="db213-103">Получает сведения о расширении Chef.</span><span class="sxs-lookup"><span data-stu-id="db213-103">Gets information about a Chef extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="db213-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="db213-104">SYNTAX</span></span>

### <span data-ttu-id="db213-105">Linux</span><span class="sxs-lookup"><span data-stu-id="db213-105">Linux</span></span>
```
Get-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-Linux] [<CommonParameters>]
```

### <span data-ttu-id="db213-106">Windows</span><span class="sxs-lookup"><span data-stu-id="db213-106">Windows</span></span>
```
Get-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-Windows] [<CommonParameters>]
```

## <span data-ttu-id="db213-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="db213-107">DESCRIPTION</span></span>
<span data-ttu-id="db213-108">Командлет **Get-AzureVMChefExtension** получает сведения о расширении Chef, установленном на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="db213-108">The **Get-AzureVMChefExtension** cmdlet gets information about a Chef extension installed on a virtual machine.</span></span>

## <span data-ttu-id="db213-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="db213-109">EXAMPLES</span></span>

### <span data-ttu-id="db213-110">Пример 1: получение подробных сведений о расширении Chef для виртуальной машины Windows</span><span class="sxs-lookup"><span data-stu-id="db213-110">Example 1: Get the details of Chef extension for a Windows virtual machine-</span></span>
```
PS C:\> Get-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -Windows
```

<span data-ttu-id="db213-111">Эта команда получает расширение Chef из виртуальной машины Windows с именем WindowsVM001, которая входит в группу ресурсов с именем ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="db213-111">This command gets the Chef extension from a Windows virtual machine named WindowsVM001 that belongs to the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="db213-112">Пример 2: получение подробных сведений о расширении Chef для виртуальной машины Linux</span><span class="sxs-lookup"><span data-stu-id="db213-112">Example 2: Get the details of Chef extension for a Linux virtual machine</span></span>
```
PS C:\> Get-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -Linux
```

<span data-ttu-id="db213-113">Эта команда получает расширение Chef из виртуальной машины Linux с именем LinuxVM001, которое принадлежит группе ресурсов с именем ResourceGroup002.</span><span class="sxs-lookup"><span data-stu-id="db213-113">This command gets the Chef extension from a Linux virtual machine named LinuxVM001 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="db213-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="db213-114">PARAMETERS</span></span>

### <span data-ttu-id="db213-115">-Linux</span><span class="sxs-lookup"><span data-stu-id="db213-115">-Linux</span></span>
<span data-ttu-id="db213-116">Указывает на то, что этот командлет работает на виртуальной машине Linux.</span><span class="sxs-lookup"><span data-stu-id="db213-116">Indicates that this cmdlet works on a Linux virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db213-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="db213-117">-Name</span></span>
<span data-ttu-id="db213-118">Указывает имя расширения Chef.</span><span class="sxs-lookup"><span data-stu-id="db213-118">Specifies the name of the Chef extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db213-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db213-119">-ResourceGroupName</span></span>
<span data-ttu-id="db213-120">Указывает имя группы ресурсов, которая содержит виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="db213-120">Specifies the name of the resource group that contains the virtual machine.</span></span>

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

### <span data-ttu-id="db213-121">-Status (состояние)</span><span class="sxs-lookup"><span data-stu-id="db213-121">-Status</span></span>
<span data-ttu-id="db213-122">Указывает на то, что этот командлет получает только представление экземпляра расширения Chef.</span><span class="sxs-lookup"><span data-stu-id="db213-122">Indicates that this cmdlet gets only the instance view of the Chef extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db213-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="db213-123">-VMName</span></span>
<span data-ttu-id="db213-124">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="db213-124">Specifies the name of a virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db213-125">-Windows</span><span class="sxs-lookup"><span data-stu-id="db213-125">-Windows</span></span>
<span data-ttu-id="db213-126">Указывает, что этот командлет предназначен для виртуальной машины Windows.</span><span class="sxs-lookup"><span data-stu-id="db213-126">Indicates that this cmdlet is for a Windows virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db213-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db213-127">CommonParameters</span></span>
<span data-ttu-id="db213-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="db213-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db213-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db213-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db213-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="db213-130">INPUTS</span></span>

### <span data-ttu-id="db213-131">Ничего</span><span class="sxs-lookup"><span data-stu-id="db213-131">None</span></span>
<span data-ttu-id="db213-132">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="db213-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="db213-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="db213-133">OUTPUTS</span></span>

## <span data-ttu-id="db213-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="db213-134">NOTES</span></span>

## <span data-ttu-id="db213-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="db213-135">RELATED LINKS</span></span>

[<span data-ttu-id="db213-136">Set-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="db213-136">Set-AzureRmVMChefExtension</span></span>](./Set-AzureRmVMChefExtension.md)

[<span data-ttu-id="db213-137">Remove-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="db213-137">Remove-AzureRmVMChefExtension</span></span>](./Remove-AzureRmVMChefExtension.md)


