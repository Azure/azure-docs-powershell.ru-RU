---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 212281F0-9A3E-4652-919F-400455E3950E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMAEMExtension.md
ms.openlocfilehash: 3d4867e33fe388195904d31fa7e83abe26dde474
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561055"
---
# <span data-ttu-id="4ffa7-101">Get-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="4ffa7-101">Get-AzureRmVMAEMExtension</span></span>

## <span data-ttu-id="4ffa7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4ffa7-102">SYNOPSIS</span></span>
<span data-ttu-id="4ffa7-103">Получает сведения о расширении AEM.</span><span class="sxs-lookup"><span data-stu-id="4ffa7-103">Gets information about the AEM extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ffa7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4ffa7-104">SYNTAX</span></span>

```
Get-AzureRmVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [[-OSType] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ffa7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4ffa7-105">DESCRIPTION</span></span>
<span data-ttu-id="4ffa7-106">Командлет **Get-AzureRmVMAEMExtension** получает сведения о расширении службы улучшенного мониторинга Azure (AEM).</span><span class="sxs-lookup"><span data-stu-id="4ffa7-106">The **Get-AzureRmVMAEMExtension** cmdlet gets information about the Azure Enhanced Monitoring (AEM) extension.</span></span>

## <span data-ttu-id="4ffa7-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4ffa7-107">EXAMPLES</span></span>

### <span data-ttu-id="4ffa7-108">Пример 1: получение расширения AEM</span><span class="sxs-lookup"><span data-stu-id="4ffa7-108">Example 1: Get the AEM extension</span></span>
```
PS C:\> Get-AzureRmVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="4ffa7-109">Эта команда получает сведения о расширении AEM для виртуальной машины с именем Contoso-Server.</span><span class="sxs-lookup"><span data-stu-id="4ffa7-109">This command gets information for the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="4ffa7-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4ffa7-110">PARAMETERS</span></span>

### <span data-ttu-id="4ffa7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ffa7-111">-DefaultProfile</span></span>
<span data-ttu-id="4ffa7-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4ffa7-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ffa7-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4ffa7-113">-Name</span></span>
<span data-ttu-id="4ffa7-114">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="4ffa7-114">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="4ffa7-115">Этот командлет получает сведения о расширении AEM на виртуальной машине, указанном этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="4ffa7-115">This cmdlet gets information for the AEM extension on the virtual machine that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="4ffa7-116">-OSType</span><span class="sxs-lookup"><span data-stu-id="4ffa7-116">-OSType</span></span>
<span data-ttu-id="4ffa7-117">Указывает тип операционной системы диска операционной системы.</span><span class="sxs-lookup"><span data-stu-id="4ffa7-117">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="4ffa7-118">Если диск операционной системы не имеет типа, необходимо указать этот параметр.</span><span class="sxs-lookup"><span data-stu-id="4ffa7-118">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="4ffa7-119">Допустимые значения этого параметра: Windows и Linux.</span><span class="sxs-lookup"><span data-stu-id="4ffa7-119">The acceptable values for this parameter are: Windows and Linux.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ffa7-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ffa7-120">-ResourceGroupName</span></span>
<span data-ttu-id="4ffa7-121">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="4ffa7-121">Specifies the name of the resource group of a virtual machine.</span></span>
<span data-ttu-id="4ffa7-122">Этот командлет получает сведения о расширении AEM на этой виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="4ffa7-122">This cmdlet gets information for the AEM extension on that virtual machine.</span></span>

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

### <span data-ttu-id="4ffa7-123">-Status (состояние)</span><span class="sxs-lookup"><span data-stu-id="4ffa7-123">-Status</span></span>
<span data-ttu-id="4ffa7-124">Указывает на то, что этот командлет получает только представление экземпляра для расширения AEM.</span><span class="sxs-lookup"><span data-stu-id="4ffa7-124">Indicates that this cmdlet gets only the instance view of the AEM extension.</span></span>

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

### <span data-ttu-id="4ffa7-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="4ffa7-125">-VMName</span></span>
<span data-ttu-id="4ffa7-126">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="4ffa7-126">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="4ffa7-127">Этот командлет получает сведения о расширении AEM для виртуальной машины, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="4ffa7-127">This cmdlet gets information about AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="4ffa7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ffa7-128">CommonParameters</span></span>
<span data-ttu-id="4ffa7-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4ffa7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ffa7-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ffa7-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ffa7-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4ffa7-131">INPUTS</span></span>

### <span data-ttu-id="4ffa7-132">System. String</span><span class="sxs-lookup"><span data-stu-id="4ffa7-132">System.String</span></span>

### <span data-ttu-id="4ffa7-133">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4ffa7-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4ffa7-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4ffa7-134">OUTPUTS</span></span>

### <span data-ttu-id="4ffa7-135">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="4ffa7-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="4ffa7-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="4ffa7-136">NOTES</span></span>

## <span data-ttu-id="4ffa7-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4ffa7-137">RELATED LINKS</span></span>

[<span data-ttu-id="4ffa7-138">Remove-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="4ffa7-138">Remove-AzureRmVMAEMExtension</span></span>](./Remove-AzureRmVMAEMExtension.md)

[<span data-ttu-id="4ffa7-139">Set-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="4ffa7-139">Set-AzureRmVMAEMExtension</span></span>](./Set-AzureRmVMAEMExtension.md)

[<span data-ttu-id="4ffa7-140">Test-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="4ffa7-140">Test-AzureRmVMAEMExtension</span></span>](./Test-AzureRmVMAEMExtension.md)


