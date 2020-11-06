---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 695F224D-DA25-49F2-916E-25DA2A48A4A7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMDscExtensionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMDscExtensionStatus.md
ms.openlocfilehash: 0a14bf4f2c8a4b686f222079cadaec1744e41d08
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567152"
---
# <span data-ttu-id="4f3ba-101">Get-AzureRmVMDscExtensionStatus</span><span class="sxs-lookup"><span data-stu-id="4f3ba-101">Get-AzureRmVMDscExtensionStatus</span></span>

## <span data-ttu-id="4f3ba-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4f3ba-102">SYNOPSIS</span></span>
<span data-ttu-id="4f3ba-103">Возвращает состояние обработчика расширений DSC для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="4f3ba-103">Gets the status of the DSC extension handler for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4f3ba-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4f3ba-104">SYNTAX</span></span>

```
Get-AzureRmVMDscExtensionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4f3ba-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4f3ba-105">DESCRIPTION</span></span>
<span data-ttu-id="4f3ba-106">Командлет **Get-AzureRmVMDscExtensionStatus** получает состояние обработчика расширения необходимой конфигурации состояния (DSC) для виртуальной машины в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4f3ba-106">The **Get-AzureRmVMDscExtensionStatus** cmdlet gets the status of the Desired State Configuration (DSC) extension handler for a virtual machine in a resource group.</span></span>
<span data-ttu-id="4f3ba-107">При применении конфигурации этот командлет создает данные, которые будут выводиться в соответствии с командлетом Start-DscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="4f3ba-107">When a configuration is applied this cmdlet produces output consistent with the Start-DscConfiguration cmdlet.</span></span>

## <span data-ttu-id="4f3ba-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4f3ba-108">EXAMPLES</span></span>

## <span data-ttu-id="4f3ba-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4f3ba-109">PARAMETERS</span></span>

### <span data-ttu-id="4f3ba-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f3ba-110">-DefaultProfile</span></span>
<span data-ttu-id="4f3ba-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4f3ba-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4f3ba-112">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4f3ba-112">-Name</span></span>
<span data-ttu-id="4f3ba-113">Указывает имя ресурса диспетчера ресурсов Azure, представляющего расширение.</span><span class="sxs-lookup"><span data-stu-id="4f3ba-113">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="4f3ba-114">Командлет Set-AzureRmVMDscExtension задает для этого имени имя Microsoft. PowerShell. DSC, которое совпадает со значением, которое используется для **Get-AzureRmVMDscExtensionStatus**.</span><span class="sxs-lookup"><span data-stu-id="4f3ba-114">The Set-AzureRmVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the same value that is used by **Get-AzureRmVMDscExtensionStatus**.</span></span>
<span data-ttu-id="4f3ba-115">Указывайте этот параметр только в том случае, если вы изменили имя по умолчанию в командлете Set или использовали другое имя ресурса в шаблоне диспетчера ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4f3ba-115">Specify this parameter only if you changed the default name in the Set cmdlet or used a different resource name in a Resource Manager template.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f3ba-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f3ba-116">-ResourceGroupName</span></span>
<span data-ttu-id="4f3ba-117">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="4f3ba-117">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="4f3ba-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="4f3ba-118">-VMName</span></span>
<span data-ttu-id="4f3ba-119">Указывает имя виртуальной машины, для которой этот командлет получает состояние расширения DSC.</span><span class="sxs-lookup"><span data-stu-id="4f3ba-119">Specifies the name of a virtual machine for which this cmdlet gets the DSC extension status.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f3ba-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f3ba-120">CommonParameters</span></span>
<span data-ttu-id="4f3ba-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4f3ba-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f3ba-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f3ba-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f3ba-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4f3ba-123">INPUTS</span></span>

## <span data-ttu-id="4f3ba-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4f3ba-124">OUTPUTS</span></span>

## <span data-ttu-id="4f3ba-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="4f3ba-125">NOTES</span></span>

## <span data-ttu-id="4f3ba-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4f3ba-126">RELATED LINKS</span></span>

[<span data-ttu-id="4f3ba-127">Set-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="4f3ba-127">Set-AzureRmVMDscExtension</span></span>](./Set-AzureRmVMDscExtension.md)


