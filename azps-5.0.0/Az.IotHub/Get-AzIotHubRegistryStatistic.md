---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubregistrystatistic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRegistryStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRegistryStatistic.md
ms.openlocfilehash: 36d59745b19df716735ce5b9b248c0ca71b7d687
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94257999"
---
# <span data-ttu-id="37ddd-101">Get-AzIotHubRegistryStatistic</span><span class="sxs-lookup"><span data-stu-id="37ddd-101">Get-AzIotHubRegistryStatistic</span></span>

## <span data-ttu-id="37ddd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="37ddd-102">SYNOPSIS</span></span>
<span data-ttu-id="37ddd-103">Возвращает RegistryStatistics для IotHub.</span><span class="sxs-lookup"><span data-stu-id="37ddd-103">Gets the RegistryStatistics for an IotHub.</span></span>

## <span data-ttu-id="37ddd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="37ddd-104">SYNTAX</span></span>

```
Get-AzIotHubRegistryStatistic [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="37ddd-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="37ddd-105">DESCRIPTION</span></span>
<span data-ttu-id="37ddd-106">Возвращает RegistryStatistics для IotHub.</span><span class="sxs-lookup"><span data-stu-id="37ddd-106">Gets the RegistryStatistics for an IotHub.</span></span>
<span data-ttu-id="37ddd-107">Это предоставляет сведения о количестве включенных и отключенных устройств в IotHub.</span><span class="sxs-lookup"><span data-stu-id="37ddd-107">This provides information about the number of total, enabled and disabled devices in an IotHub.</span></span>

## <span data-ttu-id="37ddd-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="37ddd-108">EXAMPLES</span></span>

### <span data-ttu-id="37ddd-109">Пример 1. Скачайте RegistryStatistics</span><span class="sxs-lookup"><span data-stu-id="37ddd-109">Example 1 Get the RegistryStatistics</span></span>
```
PS C:\> Get-AzIotHubRegistryStatistic -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="37ddd-110">Возвращает RegistryStatistics для IotHub с именем "myiothub"</span><span class="sxs-lookup"><span data-stu-id="37ddd-110">Gets the RegistryStatistics for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="37ddd-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="37ddd-111">PARAMETERS</span></span>

### <span data-ttu-id="37ddd-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37ddd-112">-DefaultProfile</span></span>
<span data-ttu-id="37ddd-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="37ddd-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="37ddd-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="37ddd-114">-Name</span></span>
<span data-ttu-id="37ddd-115">Имя центра Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="37ddd-115">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="37ddd-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37ddd-116">-ResourceGroupName</span></span>
<span data-ttu-id="37ddd-117">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="37ddd-117">Resource Group Name</span></span>

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

### <span data-ttu-id="37ddd-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37ddd-118">CommonParameters</span></span>
<span data-ttu-id="37ddd-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="37ddd-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37ddd-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37ddd-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37ddd-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="37ddd-121">INPUTS</span></span>

### <span data-ttu-id="37ddd-122">System. String</span><span class="sxs-lookup"><span data-stu-id="37ddd-122">System.String</span></span>

## <span data-ttu-id="37ddd-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="37ddd-123">OUTPUTS</span></span>

### <span data-ttu-id="37ddd-124">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHubRegistryStatistics</span><span class="sxs-lookup"><span data-stu-id="37ddd-124">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubRegistryStatistics</span></span>

## <span data-ttu-id="37ddd-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="37ddd-125">NOTES</span></span>

## <span data-ttu-id="37ddd-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="37ddd-126">RELATED LINKS</span></span>
