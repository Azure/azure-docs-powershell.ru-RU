---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubregistrystatistic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRegistryStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRegistryStatistic.md
ms.openlocfilehash: 36d59745b19df716735ce5b9b248c0ca71b7d687
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073825"
---
# <span data-ttu-id="993ca-101">Get-AzIotHubRegistryStatistic</span><span class="sxs-lookup"><span data-stu-id="993ca-101">Get-AzIotHubRegistryStatistic</span></span>

## <span data-ttu-id="993ca-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="993ca-102">SYNOPSIS</span></span>
<span data-ttu-id="993ca-103">Возвращает RegistryStatistics для IotHub.</span><span class="sxs-lookup"><span data-stu-id="993ca-103">Gets the RegistryStatistics for an IotHub.</span></span>

## <span data-ttu-id="993ca-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="993ca-104">SYNTAX</span></span>

```
Get-AzIotHubRegistryStatistic [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="993ca-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="993ca-105">DESCRIPTION</span></span>
<span data-ttu-id="993ca-106">Возвращает RegistryStatistics для IotHub.</span><span class="sxs-lookup"><span data-stu-id="993ca-106">Gets the RegistryStatistics for an IotHub.</span></span>
<span data-ttu-id="993ca-107">Это предоставляет сведения о количестве включенных и отключенных устройств в IotHub.</span><span class="sxs-lookup"><span data-stu-id="993ca-107">This provides information about the number of total, enabled and disabled devices in an IotHub.</span></span>

## <span data-ttu-id="993ca-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="993ca-108">EXAMPLES</span></span>

### <span data-ttu-id="993ca-109">Пример 1. Скачайте RegistryStatistics</span><span class="sxs-lookup"><span data-stu-id="993ca-109">Example 1 Get the RegistryStatistics</span></span>
```
PS C:\> Get-AzIotHubRegistryStatistic -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="993ca-110">Возвращает RegistryStatistics для IotHub с именем "myiothub"</span><span class="sxs-lookup"><span data-stu-id="993ca-110">Gets the RegistryStatistics for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="993ca-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="993ca-111">PARAMETERS</span></span>

### <span data-ttu-id="993ca-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="993ca-112">-DefaultProfile</span></span>
<span data-ttu-id="993ca-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="993ca-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="993ca-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="993ca-114">-Name</span></span>
<span data-ttu-id="993ca-115">Имя центра Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="993ca-115">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="993ca-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="993ca-116">-ResourceGroupName</span></span>
<span data-ttu-id="993ca-117">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="993ca-117">Resource Group Name</span></span>

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

### <span data-ttu-id="993ca-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="993ca-118">CommonParameters</span></span>
<span data-ttu-id="993ca-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="993ca-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="993ca-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="993ca-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="993ca-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="993ca-121">INPUTS</span></span>

### <span data-ttu-id="993ca-122">System. String</span><span class="sxs-lookup"><span data-stu-id="993ca-122">System.String</span></span>

## <span data-ttu-id="993ca-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="993ca-123">OUTPUTS</span></span>

### <span data-ttu-id="993ca-124">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHubRegistryStatistics</span><span class="sxs-lookup"><span data-stu-id="993ca-124">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubRegistryStatistics</span></span>

## <span data-ttu-id="993ca-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="993ca-125">NOTES</span></span>

## <span data-ttu-id="993ca-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="993ca-126">RELATED LINKS</span></span>
