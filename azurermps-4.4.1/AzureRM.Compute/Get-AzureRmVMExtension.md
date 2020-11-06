---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 842652D4-0F1C-4D0D-AB55-0D43D3C5D82A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMExtension.md
ms.openlocfilehash: 9ec51984a4b8291f726da81b92b1c67ea8937e5e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567148"
---
# <span data-ttu-id="c67d7-101">Get-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="c67d7-101">Get-AzureRmVMExtension</span></span>

## <span data-ttu-id="c67d7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c67d7-102">SYNOPSIS</span></span>
<span data-ttu-id="c67d7-103">Возвращает свойства расширений виртуальных машин, установленных на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="c67d7-103">Gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c67d7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c67d7-104">SYNTAX</span></span>

```
Get-AzureRmVMExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c67d7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c67d7-105">DESCRIPTION</span></span>
<span data-ttu-id="c67d7-106">Командлет **Get-AzureRmVMExtension** получает свойства расширений виртуальных машин, установленных на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="c67d7-106">The **Get-AzureRmVMExtension** cmdlet gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>
<span data-ttu-id="c67d7-107">Укажите имя расширения, для которого нужно получить свойства.</span><span class="sxs-lookup"><span data-stu-id="c67d7-107">Specify the name of an extension for which to get properties.</span></span>
<span data-ttu-id="c67d7-108">Чтобы получить только представление экземпляра расширения, укажите параметр Status.</span><span class="sxs-lookup"><span data-stu-id="c67d7-108">To get only the instance view of an extension, specify the Status parameter.</span></span>

## <span data-ttu-id="c67d7-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c67d7-109">EXAMPLES</span></span>

### <span data-ttu-id="c67d7-110">Пример 1: получение свойств расширения</span><span class="sxs-lookup"><span data-stu-id="c67d7-110">Example 1: Get properties of an extension</span></span>
```
PS C:\> Get-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22" -Name "CustomScriptExtension"
```

<span data-ttu-id="c67d7-111">Эта команда получает свойства для расширения с именем CustomScriptExtension на виртуальной машине с именем VirtualMachine22 в группе ресурсов ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="c67d7-111">This command gets properties for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

### <span data-ttu-id="c67d7-112">Пример 2: получение представления экземпляра расширения</span><span class="sxs-lookup"><span data-stu-id="c67d7-112">Example 2: Get instance view of an extension</span></span>
```
PS C:\> Get-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22" -Name "CustomScriptExtension" -Status
```

<span data-ttu-id="c67d7-113">Эта команда получает представление экземпляра для расширения с именем CustomScriptExtension на виртуальной машине с именем VirtualMachine22 в группе ресурсов ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="c67d7-113">This command gets the instance view for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="c67d7-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c67d7-114">PARAMETERS</span></span>

### <span data-ttu-id="c67d7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c67d7-115">-DefaultProfile</span></span>
<span data-ttu-id="c67d7-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c67d7-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c67d7-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c67d7-117">-Name</span></span>
<span data-ttu-id="c67d7-118">Указывает имя расширения.</span><span class="sxs-lookup"><span data-stu-id="c67d7-118">Specifies the name of an extension.</span></span>
<span data-ttu-id="c67d7-119">Этот командлет получает свойства для расширения, которое указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="c67d7-119">This cmdlet gets properties for the extension that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c67d7-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c67d7-120">-ResourceGroupName</span></span>
<span data-ttu-id="c67d7-121">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c67d7-121">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="c67d7-122">-Status (состояние)</span><span class="sxs-lookup"><span data-stu-id="c67d7-122">-Status</span></span>
<span data-ttu-id="c67d7-123">Указывает на то, что этот командлет получает только представление экземпляра расширения.</span><span class="sxs-lookup"><span data-stu-id="c67d7-123">Indicates that this cmdlet gets only the instance view of an extension.</span></span>

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

### <span data-ttu-id="c67d7-124">-VMName</span><span class="sxs-lookup"><span data-stu-id="c67d7-124">-VMName</span></span>
<span data-ttu-id="c67d7-125">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c67d7-125">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="c67d7-126">Этот командлет получает свойства расширения из виртуальной машины, указывающей этот параметр.</span><span class="sxs-lookup"><span data-stu-id="c67d7-126">This cmdlet gets properties of an extension from the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="c67d7-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c67d7-127">CommonParameters</span></span>
<span data-ttu-id="c67d7-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c67d7-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c67d7-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c67d7-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c67d7-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c67d7-130">INPUTS</span></span>

## <span data-ttu-id="c67d7-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c67d7-131">OUTPUTS</span></span>

## <span data-ttu-id="c67d7-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="c67d7-132">NOTES</span></span>

## <span data-ttu-id="c67d7-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c67d7-133">RELATED LINKS</span></span>

[<span data-ttu-id="c67d7-134">Remove-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="c67d7-134">Remove-AzureRmVMExtension</span></span>](./Remove-AzureRmVMExtension.md)

[<span data-ttu-id="c67d7-135">Set-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="c67d7-135">Set-AzureRmVMExtension</span></span>](./Set-AzureRmVMExtension.md)


