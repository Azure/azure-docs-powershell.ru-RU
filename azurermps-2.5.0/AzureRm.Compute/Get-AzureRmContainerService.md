---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: AFF75E0B-CB88-45ED-9067-7F43E2BA485C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermcontainerservice
schema: 2.0.0
ms.openlocfilehash: 5db21871b84801d57deebf98e27bbe153285631a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93915405"
---
# <span data-ttu-id="a0796-101">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="a0796-101">Get-AzureRmContainerService</span></span>

## <span data-ttu-id="a0796-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a0796-102">SYNOPSIS</span></span>
<span data-ttu-id="a0796-103">Возвращает службу контейнеров.</span><span class="sxs-lookup"><span data-stu-id="a0796-103">Gets a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a0796-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a0796-104">SYNTAX</span></span>

```
Get-AzureRmContainerService [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a0796-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a0796-105">DESCRIPTION</span></span>
<span data-ttu-id="a0796-106">Командлет **Get-AzureRmContainerService** Получает службу контейнеров.</span><span class="sxs-lookup"><span data-stu-id="a0796-106">The **Get-AzureRmContainerService** cmdlet gets a container service.</span></span>
<span data-ttu-id="a0796-107">Вы можете просматривать свойства службы контейнеров, в том числе состояние, количество основных и агентов, а также полное доменное имя главного и агента.</span><span class="sxs-lookup"><span data-stu-id="a0796-107">You can view the properties of a container service, which include state, number of master and agents, and fully qualified domain name of master and agent.</span></span>

## <span data-ttu-id="a0796-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a0796-108">EXAMPLES</span></span>

### <span data-ttu-id="a0796-109">Пример 1: получение службы контейнеров</span><span class="sxs-lookup"><span data-stu-id="a0796-109">Example 1: Get a container service</span></span>
```
PS C:\> Get-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="a0796-110">Эта команда получает службу контейнеров с именем CSResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="a0796-110">This command gets a container service named CSResourceGroup17.</span></span>

## <span data-ttu-id="a0796-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a0796-111">PARAMETERS</span></span>

### <span data-ttu-id="a0796-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0796-112">-DefaultProfile</span></span>
<span data-ttu-id="a0796-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a0796-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a0796-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a0796-114">-Name</span></span>
<span data-ttu-id="a0796-115">Указывает имя службы контейнеров, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a0796-115">Specifies the name of the container service that this cmdlet gets.</span></span>

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

### <span data-ttu-id="a0796-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0796-116">-ResourceGroupName</span></span>
<span data-ttu-id="a0796-117">Указывает группу ресурсов для службы контейнеров, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a0796-117">Specifies the resource group of the container service that this cmdlet gets.</span></span>

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

### <span data-ttu-id="a0796-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0796-118">CommonParameters</span></span>
<span data-ttu-id="a0796-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a0796-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0796-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0796-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0796-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a0796-121">INPUTS</span></span>

### <span data-ttu-id="a0796-122">Ничего</span><span class="sxs-lookup"><span data-stu-id="a0796-122">None</span></span>
<span data-ttu-id="a0796-123">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="a0796-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a0796-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a0796-124">OUTPUTS</span></span>

### <span data-ttu-id="a0796-125">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="a0796-125">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="a0796-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="a0796-126">NOTES</span></span>

## <span data-ttu-id="a0796-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a0796-127">RELATED LINKS</span></span>

[<span data-ttu-id="a0796-128">New-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="a0796-128">New-AzureRmContainerService</span></span>](./New-AzureRmContainerService.md)

[<span data-ttu-id="a0796-129">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="a0796-129">Remove-AzureRmContainerService</span></span>](./Remove-AzureRmContainerService.md)

[<span data-ttu-id="a0796-130">Update-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="a0796-130">Update-AzureRmContainerService</span></span>](./Update-AzureRmContainerService.md)


