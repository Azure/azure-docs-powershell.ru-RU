---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubKey.md
ms.openlocfilehash: 33232e5e8f415309bec36f8918c272c251835f82
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568536"
---
# <span data-ttu-id="82f49-101">Get-AzureRmIotHubKey</span><span class="sxs-lookup"><span data-stu-id="82f49-101">Get-AzureRmIotHubKey</span></span>

## <span data-ttu-id="82f49-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="82f49-102">SYNOPSIS</span></span>
<span data-ttu-id="82f49-103">Возвращает IotHub клавишу.</span><span class="sxs-lookup"><span data-stu-id="82f49-103">Gets an IotHub Key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="82f49-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="82f49-104">SYNTAX</span></span>

```
Get-AzureRmIotHubKey [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82f49-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="82f49-105">DESCRIPTION</span></span>
<span data-ttu-id="82f49-106">Возвращает IotHub клавишу.</span><span class="sxs-lookup"><span data-stu-id="82f49-106">Gets an IotHub Key.</span></span>
<span data-ttu-id="82f49-107">Вы можете либо вывести список всех ключей, либо отфильтровать список по определенному названию ключа.</span><span class="sxs-lookup"><span data-stu-id="82f49-107">You can either list all Keys or filter the list by a specific Key Name.</span></span>

## <span data-ttu-id="82f49-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="82f49-108">EXAMPLES</span></span>

### <span data-ttu-id="82f49-109">Пример 1 получить все клавиши</span><span class="sxs-lookup"><span data-stu-id="82f49-109">Example 1 Get all Keys</span></span>
```
PS C:\> Get-AzureRmIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="82f49-110">Возвращает все клавиши для IotHub с именем "myiothub"</span><span class="sxs-lookup"><span data-stu-id="82f49-110">Gets all the Keys for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="82f49-111">Пример 2 получение сведений о конкретном ключе</span><span class="sxs-lookup"><span data-stu-id="82f49-111">Example 2 Get information for a specific Key</span></span>
```
PS C:\> Get-AzureRmIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner"
```

<span data-ttu-id="82f49-112">Получает сведения для ключа с именем "iothubowner" для IotHub с именем "myiothub"</span><span class="sxs-lookup"><span data-stu-id="82f49-112">Gets the information for a key named "iothubowner" for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="82f49-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="82f49-113">PARAMETERS</span></span>

### <span data-ttu-id="82f49-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82f49-114">-DefaultProfile</span></span>
<span data-ttu-id="82f49-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="82f49-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="82f49-116">-KeyName</span><span class="sxs-lookup"><span data-stu-id="82f49-116">-KeyName</span></span>
<span data-ttu-id="82f49-117">Имя ключа</span><span class="sxs-lookup"><span data-stu-id="82f49-117">Name of the Key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82f49-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="82f49-118">-Name</span></span>
<span data-ttu-id="82f49-119">Имя центра Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="82f49-119">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="82f49-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82f49-120">-ResourceGroupName</span></span>
<span data-ttu-id="82f49-121">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="82f49-121">Resource Group Name</span></span>

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

### <span data-ttu-id="82f49-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82f49-122">CommonParameters</span></span>
<span data-ttu-id="82f49-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="82f49-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82f49-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82f49-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82f49-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="82f49-125">INPUTS</span></span>

### <span data-ttu-id="82f49-126">System. String</span><span class="sxs-lookup"><span data-stu-id="82f49-126">System.String</span></span>

## <span data-ttu-id="82f49-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="82f49-127">OUTPUTS</span></span>

### <span data-ttu-id="82f49-128">Microsoft. Azure. Commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="82f49-128">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="82f49-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="82f49-129">NOTES</span></span>

## <span data-ttu-id="82f49-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="82f49-130">RELATED LINKS</span></span>
