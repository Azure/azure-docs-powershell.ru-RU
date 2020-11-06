---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: B1CD5302-9BF0-460E-98FE-F60DFE072848
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMAEMExtension.md
ms.openlocfilehash: fb31bffbdb61c42ea1388c85b71f26af69056c54
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563672"
---
# <span data-ttu-id="62536-101">Remove-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="62536-101">Remove-AzureRmVMAEMExtension</span></span>

## <span data-ttu-id="62536-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="62536-102">SYNOPSIS</span></span>
<span data-ttu-id="62536-103">Удаляет расширение AEM из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="62536-103">Removes the AEM extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="62536-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="62536-104">SYNTAX</span></span>

```
Remove-AzureRmVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [[-OSType] <String>] [<CommonParameters>]
```

## <span data-ttu-id="62536-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="62536-105">DESCRIPTION</span></span>
<span data-ttu-id="62536-106">Командлет **Remove-AzureRmVMAEMExtension** удаляет расширение службы улучшенного мониторинга Azure (AEM) с виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="62536-106">The **Remove-AzureRmVMAEMExtension** cmdlet removes the Azure Enhanced Monitoring (AEM) extension from a virtual machine.</span></span>

## <span data-ttu-id="62536-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="62536-107">EXAMPLES</span></span>

### <span data-ttu-id="62536-108">Пример 1: удаление расширения AEM</span><span class="sxs-lookup"><span data-stu-id="62536-108">Example 1: Remove the AEM extension</span></span>
```
PS C:\> Remove-AzureRmVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="62536-109">Эта команда удаляет расширение AEM для виртуальной машины с именем Contoso-Server.</span><span class="sxs-lookup"><span data-stu-id="62536-109">This command removes the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="62536-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="62536-110">PARAMETERS</span></span>

### <span data-ttu-id="62536-111">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="62536-111">-Name</span></span>
<span data-ttu-id="62536-112">Указывает имя виртуальной машины, с помощью которой этот командлет удаляет расширение AEM.</span><span class="sxs-lookup"><span data-stu-id="62536-112">Specifies the name of the virtual machine from which this cmdlet removes the AEM extension.</span></span>

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

### <span data-ttu-id="62536-113">-OSType</span><span class="sxs-lookup"><span data-stu-id="62536-113">-OSType</span></span>
<span data-ttu-id="62536-114">Указывает тип операционной системы диска операционной системы.</span><span class="sxs-lookup"><span data-stu-id="62536-114">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="62536-115">Если диск операционной системы не имеет типа, необходимо указать этот параметр.</span><span class="sxs-lookup"><span data-stu-id="62536-115">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="62536-116">Допустимые значения этого параметра: Windows и Linux.</span><span class="sxs-lookup"><span data-stu-id="62536-116">The acceptable values for this parameter are: Windows and Linux.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62536-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62536-117">-ResourceGroupName</span></span>
<span data-ttu-id="62536-118">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="62536-118">Specifies the name of the resource group of a virtual machine.</span></span>
<span data-ttu-id="62536-119">Этот командлет удаляет расширение AEM из этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="62536-119">This cmdlet removes the AEM extension from that virtual machine.</span></span>

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

### <span data-ttu-id="62536-120">-VMName</span><span class="sxs-lookup"><span data-stu-id="62536-120">-VMName</span></span>
<span data-ttu-id="62536-121">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="62536-121">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="62536-122">Этот командлет удаляет расширение AEM для виртуальной машины, указывающей этот параметр.</span><span class="sxs-lookup"><span data-stu-id="62536-122">This cmdlet removes the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="62536-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62536-123">CommonParameters</span></span>
<span data-ttu-id="62536-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="62536-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62536-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62536-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62536-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="62536-126">INPUTS</span></span>

### <span data-ttu-id="62536-127">Ничего</span><span class="sxs-lookup"><span data-stu-id="62536-127">None</span></span>
<span data-ttu-id="62536-128">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="62536-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="62536-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="62536-129">OUTPUTS</span></span>

## <span data-ttu-id="62536-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="62536-130">NOTES</span></span>

## <span data-ttu-id="62536-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="62536-131">RELATED LINKS</span></span>

[<span data-ttu-id="62536-132">Get-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="62536-132">Get-AzureRmVMAEMExtension</span></span>](./Get-AzureRmVMAEMExtension.md)

[<span data-ttu-id="62536-133">Set-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="62536-133">Set-AzureRmVMAEMExtension</span></span>](./Set-AzureRmVMAEMExtension.md)

[<span data-ttu-id="62536-134">Test-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="62536-134">Test-AzureRmVMAEMExtension</span></span>](./Test-AzureRmVMAEMExtension.md)


