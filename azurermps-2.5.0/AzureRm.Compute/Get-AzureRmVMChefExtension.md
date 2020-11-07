---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: F41953F1-9515-4081-8624-6A1494DA4BB2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmchefextension
schema: 2.0.0
ms.openlocfilehash: e9047b681e669975e7113eb3970b2ee6573a68d5
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913673"
---
# <span data-ttu-id="1b3b5-101">Get-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="1b3b5-101">Get-AzureRmVMChefExtension</span></span>

## <span data-ttu-id="1b3b5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1b3b5-102">SYNOPSIS</span></span>
<span data-ttu-id="1b3b5-103">Получает сведения о расширении Chef.</span><span class="sxs-lookup"><span data-stu-id="1b3b5-103">Gets information about a Chef extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1b3b5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1b3b5-104">SYNTAX</span></span>

### <span data-ttu-id="1b3b5-105">Linux</span><span class="sxs-lookup"><span data-stu-id="1b3b5-105">Linux</span></span>
```
Get-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-Linux] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1b3b5-106">Windows</span><span class="sxs-lookup"><span data-stu-id="1b3b5-106">Windows</span></span>
```
Get-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-Windows] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1b3b5-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1b3b5-107">DESCRIPTION</span></span>
<span data-ttu-id="1b3b5-108">Командлет **Get-AzureVMChefExtension** получает сведения о расширении Chef, установленном на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="1b3b5-108">The **Get-AzureVMChefExtension** cmdlet gets information about a Chef extension installed on a virtual machine.</span></span>

## <span data-ttu-id="1b3b5-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1b3b5-109">EXAMPLES</span></span>

### <span data-ttu-id="1b3b5-110">Пример 1: получение подробных сведений о расширении Chef для виртуальной машины Windows</span><span class="sxs-lookup"><span data-stu-id="1b3b5-110">Example 1: Get the details of Chef extension for a Windows virtual machine-</span></span>
```
PS C:\> Get-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -Windows
```

<span data-ttu-id="1b3b5-111">Эта команда получает расширение Chef из виртуальной машины Windows с именем WindowsVM001, которая входит в группу ресурсов с именем ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="1b3b5-111">This command gets the Chef extension from a Windows virtual machine named WindowsVM001 that belongs to the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="1b3b5-112">Пример 2: получение подробных сведений о расширении Chef для виртуальной машины Linux</span><span class="sxs-lookup"><span data-stu-id="1b3b5-112">Example 2: Get the details of Chef extension for a Linux virtual machine</span></span>
```
PS C:\> Get-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -Linux
```

<span data-ttu-id="1b3b5-113">Эта команда получает расширение Chef из виртуальной машины Linux с именем LinuxVM001, которое принадлежит группе ресурсов с именем ResourceGroup002.</span><span class="sxs-lookup"><span data-stu-id="1b3b5-113">This command gets the Chef extension from a Linux virtual machine named LinuxVM001 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="1b3b5-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1b3b5-114">PARAMETERS</span></span>

### <span data-ttu-id="1b3b5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b3b5-115">-DefaultProfile</span></span>
<span data-ttu-id="1b3b5-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1b3b5-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b3b5-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="1b3b5-117">-Linux</span></span>
<span data-ttu-id="1b3b5-118">Указывает на то, что этот командлет работает на виртуальной машине Linux.</span><span class="sxs-lookup"><span data-stu-id="1b3b5-118">Indicates that this cmdlet works on a Linux virtual machine.</span></span>

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

### <span data-ttu-id="1b3b5-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1b3b5-119">-Name</span></span>
<span data-ttu-id="1b3b5-120">Указывает имя расширения Chef.</span><span class="sxs-lookup"><span data-stu-id="1b3b5-120">Specifies the name of the Chef extension.</span></span>

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

### <span data-ttu-id="1b3b5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b3b5-121">-ResourceGroupName</span></span>
<span data-ttu-id="1b3b5-122">Указывает имя группы ресурсов, которая содержит виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="1b3b5-122">Specifies the name of the resource group that contains the virtual machine.</span></span>

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

### <span data-ttu-id="1b3b5-123">-Status (состояние)</span><span class="sxs-lookup"><span data-stu-id="1b3b5-123">-Status</span></span>
<span data-ttu-id="1b3b5-124">Указывает на то, что этот командлет получает только представление экземпляра расширения Chef.</span><span class="sxs-lookup"><span data-stu-id="1b3b5-124">Indicates that this cmdlet gets only the instance view of the Chef extension.</span></span>

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

### <span data-ttu-id="1b3b5-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="1b3b5-125">-VMName</span></span>
<span data-ttu-id="1b3b5-126">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="1b3b5-126">Specifies the name of a virtual machine.</span></span>

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

### <span data-ttu-id="1b3b5-127">-Windows</span><span class="sxs-lookup"><span data-stu-id="1b3b5-127">-Windows</span></span>
<span data-ttu-id="1b3b5-128">Указывает, что этот командлет предназначен для виртуальной машины Windows.</span><span class="sxs-lookup"><span data-stu-id="1b3b5-128">Indicates that this cmdlet is for a Windows virtual machine.</span></span>

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

### <span data-ttu-id="1b3b5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b3b5-129">CommonParameters</span></span>
<span data-ttu-id="1b3b5-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1b3b5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b3b5-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b3b5-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b3b5-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1b3b5-132">INPUTS</span></span>

### <span data-ttu-id="1b3b5-133">Ничего</span><span class="sxs-lookup"><span data-stu-id="1b3b5-133">None</span></span>
<span data-ttu-id="1b3b5-134">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="1b3b5-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1b3b5-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1b3b5-135">OUTPUTS</span></span>

### <span data-ttu-id="1b3b5-136">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="1b3b5-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="1b3b5-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="1b3b5-137">NOTES</span></span>

## <span data-ttu-id="1b3b5-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1b3b5-138">RELATED LINKS</span></span>

[<span data-ttu-id="1b3b5-139">Set-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="1b3b5-139">Set-AzureRmVMChefExtension</span></span>](./Set-AzureRmVMChefExtension.md)

[<span data-ttu-id="1b3b5-140">Remove-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="1b3b5-140">Remove-AzureRmVMChefExtension</span></span>](./Remove-AzureRmVMChefExtension.md)


