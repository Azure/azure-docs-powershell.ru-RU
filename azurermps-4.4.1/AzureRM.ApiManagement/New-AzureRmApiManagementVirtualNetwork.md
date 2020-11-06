---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: FB5E4ED2-8EF3-462F-A053-7EC82C767E8D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementVirtualNetwork.md
ms.openlocfilehash: 42213ddd4a7780b4d69b357c4b801df34aa9aca4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558024"
---
# <span data-ttu-id="8f531-101">New-AzureRmApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="8f531-101">New-AzureRmApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="8f531-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8f531-102">SYNOPSIS</span></span>
<span data-ttu-id="8f531-103">Создает экземпляр PsApiManagementVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="8f531-103">Creates an instance of PsApiManagementVirtualNetwork.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f531-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8f531-104">SYNTAX</span></span>

```
New-AzureRmApiManagementVirtualNetwork -Location <String> -SubnetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8f531-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8f531-105">DESCRIPTION</span></span>
<span data-ttu-id="8f531-106">Командлет **New-AzureRmApiManagementVirtualNetwork** является вспомогательной командой для создания экземпляра **PsApiManagementVirtualNetwork**.</span><span class="sxs-lookup"><span data-stu-id="8f531-106">The **New-AzureRmApiManagementVirtualNetwork** cmdlet is a helper command to create an instance of **PsApiManagementVirtualNetwork**.</span></span>
<span data-ttu-id="8f531-107">Эта команда используется с командлетом **Set-AzureRMApiManagementVirtualNetworks** .</span><span class="sxs-lookup"><span data-stu-id="8f531-107">This command is used with **Set-AzureRMApiManagementVirtualNetworks** cmdlet.</span></span>

## <span data-ttu-id="8f531-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8f531-108">EXAMPLES</span></span>

### <span data-ttu-id="8f531-109">Пример 1: создание виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="8f531-109">Example 1: Create a virtual network</span></span>
```
PS C:\>$VirtualNetworks = @()
PS C:\> $VirtualNetworks += New-AzureRmApiManagementVirtualNetwork -Location "East US" -SubtenName "ContosoNet" -VnetId "089D3F4D-B986-4DFD-9259-9112BA7A1F03"
PS C:\> Set-AzureRmApiManagementVirtualNetworks -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetworks $VirtualNetworks
```

<span data-ttu-id="8f531-110">В этом примере создается виртуальная сеть и затем вызывается командлет **Set-AzureRmApiManagementVirtualNetworks** .</span><span class="sxs-lookup"><span data-stu-id="8f531-110">This example creates a virtual network and then calls the **Set-AzureRmApiManagementVirtualNetworks** cmdlet.</span></span>

## <span data-ttu-id="8f531-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8f531-111">PARAMETERS</span></span>

### <span data-ttu-id="8f531-112">-Location</span><span class="sxs-lookup"><span data-stu-id="8f531-112">-Location</span></span>
<span data-ttu-id="8f531-113">Указывает расположение виртуальной сети, в которой этот командлет создает экземпляр.</span><span class="sxs-lookup"><span data-stu-id="8f531-113">Specifies the location of the virtual network in which this cmdlet creates the instance.</span></span>

<span data-ttu-id="8f531-114">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="8f531-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8f531-115">Северный Центральный США</span><span class="sxs-lookup"><span data-stu-id="8f531-115">North Central US</span></span>
- <span data-ttu-id="8f531-116">Южная Центральная американская</span><span class="sxs-lookup"><span data-stu-id="8f531-116">South Central US</span></span>
- <span data-ttu-id="8f531-117">Центральная американская</span><span class="sxs-lookup"><span data-stu-id="8f531-117">Central US</span></span>
- <span data-ttu-id="8f531-118">Западная Европа</span><span class="sxs-lookup"><span data-stu-id="8f531-118">West Europe</span></span>
- <span data-ttu-id="8f531-119">Северная Европа</span><span class="sxs-lookup"><span data-stu-id="8f531-119">North Europe</span></span>
- <span data-ttu-id="8f531-120">Западная часть США</span><span class="sxs-lookup"><span data-stu-id="8f531-120">West US</span></span>
- <span data-ttu-id="8f531-121">Восточная часть США</span><span class="sxs-lookup"><span data-stu-id="8f531-121">East US</span></span>
- <span data-ttu-id="8f531-122">Восточная часть 2</span><span class="sxs-lookup"><span data-stu-id="8f531-122">East US 2</span></span>
- <span data-ttu-id="8f531-123">Восточная Япония</span><span class="sxs-lookup"><span data-stu-id="8f531-123">Japan East</span></span>
- <span data-ttu-id="8f531-124">Западная часть Японии</span><span class="sxs-lookup"><span data-stu-id="8f531-124">Japan West</span></span>
- <span data-ttu-id="8f531-125">Южная Бразилия</span><span class="sxs-lookup"><span data-stu-id="8f531-125">Brazil South</span></span>
- <span data-ttu-id="8f531-126">Юго-Восточная Азия</span><span class="sxs-lookup"><span data-stu-id="8f531-126">Southeast Asia</span></span>
- <span data-ttu-id="8f531-127">Восточная Азия</span><span class="sxs-lookup"><span data-stu-id="8f531-127">East Asia</span></span>
- <span data-ttu-id="8f531-128">Восточная Австралия</span><span class="sxs-lookup"><span data-stu-id="8f531-128">Australia East</span></span>
- <span data-ttu-id="8f531-129">Юго-восток Австралии</span><span class="sxs-lookup"><span data-stu-id="8f531-129">Australia Southeast</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f531-130">-SubnetResourceId</span><span class="sxs-lookup"><span data-stu-id="8f531-130">-SubnetResourceId</span></span>
<span data-ttu-id="8f531-131">Указывает идентификатор ресурса подсети виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="8f531-131">Specifies the subnet resource ID of the virtual network.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f531-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f531-132">-DefaultProfile</span></span>
<span data-ttu-id="8f531-133">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8f531-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8f531-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f531-134">CommonParameters</span></span>
<span data-ttu-id="8f531-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8f531-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f531-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f531-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f531-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8f531-137">INPUTS</span></span>

## <span data-ttu-id="8f531-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8f531-138">OUTPUTS</span></span>

### <span data-ttu-id="8f531-139">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="8f531-139">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="8f531-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="8f531-140">NOTES</span></span>

## <span data-ttu-id="8f531-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8f531-141">RELATED LINKS</span></span>

