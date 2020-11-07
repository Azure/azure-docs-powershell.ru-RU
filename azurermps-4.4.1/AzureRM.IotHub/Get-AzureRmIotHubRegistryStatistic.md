---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubRegistryStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubRegistryStatistic.md
ms.openlocfilehash: 033a7be2da102274837c881337fcb8f5bca4b879
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733365"
---
# <span data-ttu-id="8f684-101">Get-AzureRmIotHubRegistryStatistic</span><span class="sxs-lookup"><span data-stu-id="8f684-101">Get-AzureRmIotHubRegistryStatistic</span></span>

## <span data-ttu-id="8f684-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8f684-102">SYNOPSIS</span></span>
<span data-ttu-id="8f684-103">Возвращает RegistryStatistics для IotHub.</span><span class="sxs-lookup"><span data-stu-id="8f684-103">Gets the RegistryStatistics for an IotHub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f684-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8f684-104">SYNTAX</span></span>

```
Get-AzureRmIotHubRegistryStatistic [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8f684-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8f684-105">DESCRIPTION</span></span>
<span data-ttu-id="8f684-106">Возвращает RegistryStatistics для IotHub.</span><span class="sxs-lookup"><span data-stu-id="8f684-106">Gets the RegistryStatistics for an IotHub.</span></span>
<span data-ttu-id="8f684-107">Это предоставляет сведения о количестве включенных и отключенных устройств в IotHub.</span><span class="sxs-lookup"><span data-stu-id="8f684-107">This provides information about the number of total, enabled and disabled devices in an IotHub.</span></span>

## <span data-ttu-id="8f684-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8f684-108">EXAMPLES</span></span>

### <span data-ttu-id="8f684-109">Пример 1. Скачайте RegistryStatistics</span><span class="sxs-lookup"><span data-stu-id="8f684-109">Example 1 Get the RegistryStatistics</span></span>
```
PS C:\> Get-AzureRmIotHubRegistryStatistic -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="8f684-110">Возвращает RegistryStatictics для IotHub с именем "myiothub"</span><span class="sxs-lookup"><span data-stu-id="8f684-110">Gets the RegistryStatictics for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="8f684-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8f684-111">PARAMETERS</span></span>

### <span data-ttu-id="8f684-112">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8f684-112">-Name</span></span>
<span data-ttu-id="8f684-113">Имя центра Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="8f684-113">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="8f684-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f684-114">-ResourceGroupName</span></span>
<span data-ttu-id="8f684-115">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="8f684-115">Resource Group Name</span></span>

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

### <span data-ttu-id="8f684-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f684-116">-DefaultProfile</span></span>
<span data-ttu-id="8f684-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8f684-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8f684-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f684-118">CommonParameters</span></span>
<span data-ttu-id="8f684-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8f684-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f684-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f684-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f684-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8f684-121">INPUTS</span></span>

### <span data-ttu-id="8f684-122">System. String</span><span class="sxs-lookup"><span data-stu-id="8f684-122">System.String</span></span>

## <span data-ttu-id="8f684-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8f684-123">OUTPUTS</span></span>

### <span data-ttu-id="8f684-124">System. Collections. Generic. IList ' 1 [[Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHubRegistryStatistics, Microsoft. Azure. Commands. IotHub, Version = 1.0.0.0, Culture = "нейтрально", PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="8f684-124">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubRegistryStatistics, Microsoft.Azure.Commands.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="8f684-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="8f684-125">NOTES</span></span>

## <span data-ttu-id="8f684-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8f684-126">RELATED LINKS</span></span>

