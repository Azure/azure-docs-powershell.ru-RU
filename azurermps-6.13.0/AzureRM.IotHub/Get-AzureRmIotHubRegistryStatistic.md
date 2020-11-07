---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubregistrystatistic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubRegistryStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubRegistryStatistic.md
ms.openlocfilehash: a472ce25d648a70d9f47b6268b6bdf4f606f2a08
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734390"
---
# <span data-ttu-id="36a44-101">Get-AzureRmIotHubRegistryStatistic</span><span class="sxs-lookup"><span data-stu-id="36a44-101">Get-AzureRmIotHubRegistryStatistic</span></span>

## <span data-ttu-id="36a44-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="36a44-102">SYNOPSIS</span></span>
<span data-ttu-id="36a44-103">Возвращает RegistryStatistics для IotHub.</span><span class="sxs-lookup"><span data-stu-id="36a44-103">Gets the RegistryStatistics for an IotHub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36a44-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="36a44-104">SYNTAX</span></span>

```
Get-AzureRmIotHubRegistryStatistic [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="36a44-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="36a44-105">DESCRIPTION</span></span>
<span data-ttu-id="36a44-106">Возвращает RegistryStatistics для IotHub.</span><span class="sxs-lookup"><span data-stu-id="36a44-106">Gets the RegistryStatistics for an IotHub.</span></span>
<span data-ttu-id="36a44-107">Это предоставляет сведения о количестве включенных и отключенных устройств в IotHub.</span><span class="sxs-lookup"><span data-stu-id="36a44-107">This provides information about the number of total, enabled and disabled devices in an IotHub.</span></span>

## <span data-ttu-id="36a44-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="36a44-108">EXAMPLES</span></span>

### <span data-ttu-id="36a44-109">Пример 1. Скачайте RegistryStatistics</span><span class="sxs-lookup"><span data-stu-id="36a44-109">Example 1 Get the RegistryStatistics</span></span>
```
PS C:\> Get-AzureRmIotHubRegistryStatistic -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="36a44-110">Возвращает RegistryStatictics для IotHub с именем "myiothub"</span><span class="sxs-lookup"><span data-stu-id="36a44-110">Gets the RegistryStatictics for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="36a44-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="36a44-111">PARAMETERS</span></span>

### <span data-ttu-id="36a44-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36a44-112">-DefaultProfile</span></span>
<span data-ttu-id="36a44-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="36a44-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="36a44-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="36a44-114">-Name</span></span>
<span data-ttu-id="36a44-115">Имя центра Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="36a44-115">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="36a44-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36a44-116">-ResourceGroupName</span></span>
<span data-ttu-id="36a44-117">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="36a44-117">Resource Group Name</span></span>

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

### <span data-ttu-id="36a44-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36a44-118">CommonParameters</span></span>
<span data-ttu-id="36a44-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="36a44-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36a44-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36a44-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36a44-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="36a44-121">INPUTS</span></span>

### <span data-ttu-id="36a44-122">System. String</span><span class="sxs-lookup"><span data-stu-id="36a44-122">System.String</span></span>

## <span data-ttu-id="36a44-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="36a44-123">OUTPUTS</span></span>

### <span data-ttu-id="36a44-124">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHubRegistryStatistics</span><span class="sxs-lookup"><span data-stu-id="36a44-124">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubRegistryStatistics</span></span>

## <span data-ttu-id="36a44-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="36a44-125">NOTES</span></span>

## <span data-ttu-id="36a44-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="36a44-126">RELATED LINKS</span></span>
