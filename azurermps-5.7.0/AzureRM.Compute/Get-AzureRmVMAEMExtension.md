---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 212281F0-9A3E-4652-919F-400455E3950E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMAEMExtension.md
ms.openlocfilehash: 3970d26199fc122f248ad8e41a5146222cad23e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734482"
---
# <span data-ttu-id="be956-101">Get-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="be956-101">Get-AzureRmVMAEMExtension</span></span>

## <span data-ttu-id="be956-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="be956-102">SYNOPSIS</span></span>
<span data-ttu-id="be956-103">Получает сведения о расширении AEM.</span><span class="sxs-lookup"><span data-stu-id="be956-103">Gets information about the AEM extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="be956-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="be956-104">SYNTAX</span></span>

```
Get-AzureRmVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [[-OSType] <String>] [<CommonParameters>]
```

## <span data-ttu-id="be956-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="be956-105">DESCRIPTION</span></span>
<span data-ttu-id="be956-106">Командлет **Get-AzureRmVMAEMExtension** получает сведения о расширении службы улучшенного мониторинга Azure (AEM).</span><span class="sxs-lookup"><span data-stu-id="be956-106">The **Get-AzureRmVMAEMExtension** cmdlet gets information about the Azure Enhanced Monitoring (AEM) extension.</span></span>

## <span data-ttu-id="be956-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="be956-107">EXAMPLES</span></span>

### <span data-ttu-id="be956-108">Пример 1: получение расширения AEM</span><span class="sxs-lookup"><span data-stu-id="be956-108">Example 1: Get the AEM extension</span></span>
```
PS C:\> Get-AzureRmVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="be956-109">Эта команда получает сведения о расширении AEM для виртуальной машины с именем Contoso-Server.</span><span class="sxs-lookup"><span data-stu-id="be956-109">This command gets information for the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="be956-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="be956-110">PARAMETERS</span></span>

### <span data-ttu-id="be956-111">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="be956-111">-Name</span></span>
<span data-ttu-id="be956-112">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="be956-112">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="be956-113">Этот командлет получает сведения о расширении AEM на виртуальной машине, указанном этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="be956-113">This cmdlet gets information for the AEM extension on the virtual machine that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="be956-114">-OSType</span><span class="sxs-lookup"><span data-stu-id="be956-114">-OSType</span></span>
<span data-ttu-id="be956-115">Указывает тип операционной системы диска операционной системы.</span><span class="sxs-lookup"><span data-stu-id="be956-115">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="be956-116">Если диск операционной системы не имеет типа, необходимо указать этот параметр.</span><span class="sxs-lookup"><span data-stu-id="be956-116">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="be956-117">Допустимые значения этого параметра: Windows и Linux.</span><span class="sxs-lookup"><span data-stu-id="be956-117">The acceptable values for this parameter are: Windows and Linux.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be956-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be956-118">-ResourceGroupName</span></span>
<span data-ttu-id="be956-119">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="be956-119">Specifies the name of the resource group of a virtual machine.</span></span>
<span data-ttu-id="be956-120">Этот командлет получает сведения о расширении AEM на этой виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="be956-120">This cmdlet gets information for the AEM extension on that virtual machine.</span></span>

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

### <span data-ttu-id="be956-121">-Status (состояние)</span><span class="sxs-lookup"><span data-stu-id="be956-121">-Status</span></span>
<span data-ttu-id="be956-122">Указывает на то, что этот командлет получает только представление экземпляра для расширения AEM.</span><span class="sxs-lookup"><span data-stu-id="be956-122">Indicates that this cmdlet gets only the instance view of the AEM extension.</span></span>

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

### <span data-ttu-id="be956-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="be956-123">-VMName</span></span>
<span data-ttu-id="be956-124">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="be956-124">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="be956-125">Этот командлет получает сведения о расширении AEM для виртуальной машины, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="be956-125">This cmdlet gets information about AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="be956-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be956-126">CommonParameters</span></span>
<span data-ttu-id="be956-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="be956-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be956-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be956-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be956-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="be956-129">INPUTS</span></span>

### <span data-ttu-id="be956-130">Ничего</span><span class="sxs-lookup"><span data-stu-id="be956-130">None</span></span>
<span data-ttu-id="be956-131">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="be956-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="be956-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="be956-132">OUTPUTS</span></span>

## <span data-ttu-id="be956-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="be956-133">NOTES</span></span>

## <span data-ttu-id="be956-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="be956-134">RELATED LINKS</span></span>

[<span data-ttu-id="be956-135">Remove-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="be956-135">Remove-AzureRmVMAEMExtension</span></span>](./Remove-AzureRmVMAEMExtension.md)

[<span data-ttu-id="be956-136">Set-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="be956-136">Set-AzureRmVMAEMExtension</span></span>](./Set-AzureRmVMAEMExtension.md)

[<span data-ttu-id="be956-137">Test-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="be956-137">Test-AzureRmVMAEMExtension</span></span>](./Test-AzureRmVMAEMExtension.md)


