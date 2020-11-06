---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubregistrystatistic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubRegistryStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubRegistryStatistic.md
ms.openlocfilehash: d9c53652dab75b342dbf410cae8e8968534afcc9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568583"
---
# <span data-ttu-id="98dad-101">Get-AzureRmIotHubRegistryStatistic</span><span class="sxs-lookup"><span data-stu-id="98dad-101">Get-AzureRmIotHubRegistryStatistic</span></span>

## <span data-ttu-id="98dad-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="98dad-102">SYNOPSIS</span></span>
<span data-ttu-id="98dad-103">Возвращает RegistryStatistics для IotHub.</span><span class="sxs-lookup"><span data-stu-id="98dad-103">Gets the RegistryStatistics for an IotHub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="98dad-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="98dad-104">SYNTAX</span></span>

```
Get-AzureRmIotHubRegistryStatistic [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98dad-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="98dad-105">DESCRIPTION</span></span>
<span data-ttu-id="98dad-106">Возвращает RegistryStatistics для IotHub.</span><span class="sxs-lookup"><span data-stu-id="98dad-106">Gets the RegistryStatistics for an IotHub.</span></span>
<span data-ttu-id="98dad-107">Это предоставляет сведения о количестве включенных и отключенных устройств в IotHub.</span><span class="sxs-lookup"><span data-stu-id="98dad-107">This provides information about the number of total, enabled and disabled devices in an IotHub.</span></span>

## <span data-ttu-id="98dad-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="98dad-108">EXAMPLES</span></span>

### <span data-ttu-id="98dad-109">Пример 1. Скачайте RegistryStatistics</span><span class="sxs-lookup"><span data-stu-id="98dad-109">Example 1 Get the RegistryStatistics</span></span>
```
PS C:\> Get-AzureRmIotHubRegistryStatistic -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="98dad-110">Возвращает RegistryStatictics для IotHub с именем "myiothub"</span><span class="sxs-lookup"><span data-stu-id="98dad-110">Gets the RegistryStatictics for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="98dad-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="98dad-111">PARAMETERS</span></span>

### <span data-ttu-id="98dad-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98dad-112">-DefaultProfile</span></span>
<span data-ttu-id="98dad-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="98dad-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="98dad-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="98dad-114">-Name</span></span>
<span data-ttu-id="98dad-115">Имя центра Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="98dad-115">Name of the IoT hub.</span></span> 

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98dad-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98dad-116">-ResourceGroupName</span></span>
<span data-ttu-id="98dad-117">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="98dad-117">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98dad-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98dad-118">CommonParameters</span></span>
<span data-ttu-id="98dad-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="98dad-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98dad-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98dad-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98dad-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="98dad-121">INPUTS</span></span>

### <span data-ttu-id="98dad-122">System. String</span><span class="sxs-lookup"><span data-stu-id="98dad-122">System.String</span></span>

## <span data-ttu-id="98dad-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="98dad-123">OUTPUTS</span></span>

### <span data-ttu-id="98dad-124">System. Collections. Generic. IList ' 1 [[Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHubRegistryStatistics, Microsoft. Azure. Commands. IotHub, Version = 1.0.0.0, Culture = "нейтрально", PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="98dad-124">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubRegistryStatistics, Microsoft.Azure.Commands.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="98dad-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="98dad-125">NOTES</span></span>

## <span data-ttu-id="98dad-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="98dad-126">RELATED LINKS</span></span>

