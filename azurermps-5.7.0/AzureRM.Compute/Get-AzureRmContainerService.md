---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: AFF75E0B-CB88-45ED-9067-7F43E2BA485C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmContainerService.md
ms.openlocfilehash: d2a53d221adf7483899056791aefd00b03aca26e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565574"
---
# <span data-ttu-id="63e0e-101">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="63e0e-101">Get-AzureRmContainerService</span></span>

## <span data-ttu-id="63e0e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="63e0e-102">SYNOPSIS</span></span>
<span data-ttu-id="63e0e-103">Возвращает службу контейнеров.</span><span class="sxs-lookup"><span data-stu-id="63e0e-103">Gets a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="63e0e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="63e0e-104">SYNTAX</span></span>

```
Get-AzureRmContainerService [[-ResourceGroupName] <String>] [[-Name] <String>] [<CommonParameters>]
```

## <span data-ttu-id="63e0e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="63e0e-105">DESCRIPTION</span></span>
<span data-ttu-id="63e0e-106">Командлет **Get-AzureRmContainerService** Получает службу контейнеров.</span><span class="sxs-lookup"><span data-stu-id="63e0e-106">The **Get-AzureRmContainerService** cmdlet gets a container service.</span></span>
<span data-ttu-id="63e0e-107">Вы можете просматривать свойства службы контейнеров, в том числе состояние, количество основных и агентов, а также полное доменное имя главного и агента.</span><span class="sxs-lookup"><span data-stu-id="63e0e-107">You can view the properties of a container service, which include state, number of master and agents, and fully qualified domain name of master and agent.</span></span>

## <span data-ttu-id="63e0e-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="63e0e-108">EXAMPLES</span></span>

### <span data-ttu-id="63e0e-109">Пример 1: получение службы контейнеров</span><span class="sxs-lookup"><span data-stu-id="63e0e-109">Example 1: Get a container service</span></span>
```
PS C:\> Get-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="63e0e-110">Эта команда получает службу контейнеров с именем CSResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="63e0e-110">This command gets a container service named CSResourceGroup17.</span></span>

## <span data-ttu-id="63e0e-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="63e0e-111">PARAMETERS</span></span>

### <span data-ttu-id="63e0e-112">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="63e0e-112">-Name</span></span>
<span data-ttu-id="63e0e-113">Указывает имя службы контейнеров, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="63e0e-113">Specifies the name of the container service that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63e0e-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63e0e-114">-ResourceGroupName</span></span>
<span data-ttu-id="63e0e-115">Указывает группу ресурсов для службы контейнеров, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="63e0e-115">Specifies the resource group of the container service that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63e0e-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63e0e-116">CommonParameters</span></span>
<span data-ttu-id="63e0e-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="63e0e-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63e0e-118">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63e0e-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63e0e-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="63e0e-119">INPUTS</span></span>

### <span data-ttu-id="63e0e-120">Ничего</span><span class="sxs-lookup"><span data-stu-id="63e0e-120">None</span></span>
<span data-ttu-id="63e0e-121">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="63e0e-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="63e0e-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="63e0e-122">OUTPUTS</span></span>

## <span data-ttu-id="63e0e-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="63e0e-123">NOTES</span></span>

## <span data-ttu-id="63e0e-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="63e0e-124">RELATED LINKS</span></span>

[<span data-ttu-id="63e0e-125">New-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="63e0e-125">New-AzureRmContainerService</span></span>](./New-AzureRmContainerService.md)

[<span data-ttu-id="63e0e-126">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="63e0e-126">Remove-AzureRmContainerService</span></span>](./Remove-AzureRmContainerService.md)

[<span data-ttu-id="63e0e-127">Update-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="63e0e-127">Update-AzureRmContainerService</span></span>](./Update-AzureRmContainerService.md)


