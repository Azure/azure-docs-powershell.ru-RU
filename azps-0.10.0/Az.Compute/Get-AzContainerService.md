---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: AFF75E0B-CB88-45ED-9067-7F43E2BA485C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzContainerService.md
ms.openlocfilehash: 1a0daa4bf336ba970c12c24db3d5aab73641aaea
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911559"
---
# <span data-ttu-id="a7781-101">Get-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="a7781-101">Get-AzContainerService</span></span>

## <span data-ttu-id="a7781-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a7781-102">SYNOPSIS</span></span>
<span data-ttu-id="a7781-103">Возвращает службу контейнеров.</span><span class="sxs-lookup"><span data-stu-id="a7781-103">Gets a container service.</span></span>

## <span data-ttu-id="a7781-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a7781-104">SYNTAX</span></span>

```
Get-AzContainerService [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a7781-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a7781-105">DESCRIPTION</span></span>
<span data-ttu-id="a7781-106">Командлет **Get-AzContainerService** Получает службу контейнеров.</span><span class="sxs-lookup"><span data-stu-id="a7781-106">The **Get-AzContainerService** cmdlet gets a container service.</span></span>
<span data-ttu-id="a7781-107">Вы можете просматривать свойства службы контейнеров, в том числе состояние, количество основных и агентов, а также полное доменное имя главного и агента.</span><span class="sxs-lookup"><span data-stu-id="a7781-107">You can view the properties of a container service, which include state, number of master and agents, and fully qualified domain name of master and agent.</span></span>

## <span data-ttu-id="a7781-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a7781-108">EXAMPLES</span></span>

### <span data-ttu-id="a7781-109">Пример 1: получение службы контейнеров</span><span class="sxs-lookup"><span data-stu-id="a7781-109">Example 1: Get a container service</span></span>
```
PS C:\> Get-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="a7781-110">Эта команда получает службу контейнеров с именем CSResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="a7781-110">This command gets a container service named CSResourceGroup17.</span></span>

## <span data-ttu-id="a7781-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a7781-111">PARAMETERS</span></span>

### <span data-ttu-id="a7781-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7781-112">-DefaultProfile</span></span>
<span data-ttu-id="a7781-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a7781-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7781-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a7781-114">-Name</span></span>
<span data-ttu-id="a7781-115">Указывает имя службы контейнеров, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a7781-115">Specifies the name of the container service that this cmdlet gets.</span></span>

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

### <span data-ttu-id="a7781-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7781-116">-ResourceGroupName</span></span>
<span data-ttu-id="a7781-117">Указывает группу ресурсов для службы контейнеров, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a7781-117">Specifies the resource group of the container service that this cmdlet gets.</span></span>

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

### <span data-ttu-id="a7781-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7781-118">CommonParameters</span></span>
<span data-ttu-id="a7781-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a7781-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7781-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7781-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7781-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a7781-121">INPUTS</span></span>

### <span data-ttu-id="a7781-122">Ничего</span><span class="sxs-lookup"><span data-stu-id="a7781-122">None</span></span>
<span data-ttu-id="a7781-123">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="a7781-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a7781-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a7781-124">OUTPUTS</span></span>

### <span data-ttu-id="a7781-125">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="a7781-125">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="a7781-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="a7781-126">NOTES</span></span>

## <span data-ttu-id="a7781-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a7781-127">RELATED LINKS</span></span>

[<span data-ttu-id="a7781-128">New-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="a7781-128">New-AzContainerService</span></span>](./New-AzContainerService.md)

[<span data-ttu-id="a7781-129">Remove-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="a7781-129">Remove-AzContainerService</span></span>](./Remove-AzContainerService.md)

[<span data-ttu-id="a7781-130">Update-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="a7781-130">Update-AzContainerService</span></span>](./Update-AzContainerService.md)


