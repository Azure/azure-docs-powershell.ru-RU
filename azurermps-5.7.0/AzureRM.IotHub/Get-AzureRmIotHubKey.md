---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubKey.md
ms.openlocfilehash: 2f780b87da605a0b4c31e68b5d302cc486f78a1c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564867"
---
# <span data-ttu-id="89e79-101">Get-AzureRmIotHubKey</span><span class="sxs-lookup"><span data-stu-id="89e79-101">Get-AzureRmIotHubKey</span></span>

## <span data-ttu-id="89e79-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="89e79-102">SYNOPSIS</span></span>
<span data-ttu-id="89e79-103">Возвращает IotHub клавишу.</span><span class="sxs-lookup"><span data-stu-id="89e79-103">Gets an IotHub Key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="89e79-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="89e79-104">SYNTAX</span></span>

```
Get-AzureRmIotHubKey [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89e79-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="89e79-105">DESCRIPTION</span></span>
<span data-ttu-id="89e79-106">Возвращает IotHub клавишу.</span><span class="sxs-lookup"><span data-stu-id="89e79-106">Gets an IotHub Key.</span></span>
<span data-ttu-id="89e79-107">Вы можете либо вывести список всех ключей, либо отфильтровать список по определенному названию ключа.</span><span class="sxs-lookup"><span data-stu-id="89e79-107">You can either list all Keys or filter the list by a specific Key Name.</span></span>

## <span data-ttu-id="89e79-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="89e79-108">EXAMPLES</span></span>

### <span data-ttu-id="89e79-109">Пример 1 получить все клавиши</span><span class="sxs-lookup"><span data-stu-id="89e79-109">Example 1 Get all Keys</span></span>
```
PS C:\> Get-AzureRmIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="89e79-110">Возвращает все клавиши для IotHub с именем "myiothub"</span><span class="sxs-lookup"><span data-stu-id="89e79-110">Gets all the Keys for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="89e79-111">Пример 2 получение сведений о конкретном ключе</span><span class="sxs-lookup"><span data-stu-id="89e79-111">Example 2 Get information for a specific Key</span></span>
```
PS C:\> Get-AzureRmIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner"
```

<span data-ttu-id="89e79-112">Получает сведения для ключа с именем "iothubowner" для IotHub с именем "myiothub"</span><span class="sxs-lookup"><span data-stu-id="89e79-112">Gets the information for a key named "iothubowner" for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="89e79-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="89e79-113">PARAMETERS</span></span>

### <span data-ttu-id="89e79-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89e79-114">-DefaultProfile</span></span>
<span data-ttu-id="89e79-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="89e79-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="89e79-116">-KeyName</span><span class="sxs-lookup"><span data-stu-id="89e79-116">-KeyName</span></span>
<span data-ttu-id="89e79-117">Имя ключа</span><span class="sxs-lookup"><span data-stu-id="89e79-117">Name of the Key</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89e79-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="89e79-118">-Name</span></span>
<span data-ttu-id="89e79-119">Имя центра Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="89e79-119">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="89e79-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89e79-120">-ResourceGroupName</span></span>
<span data-ttu-id="89e79-121">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="89e79-121">Resource Group Name</span></span>

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

### <span data-ttu-id="89e79-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89e79-122">CommonParameters</span></span>
<span data-ttu-id="89e79-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="89e79-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89e79-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89e79-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89e79-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="89e79-125">INPUTS</span></span>

### <span data-ttu-id="89e79-126">System. String</span><span class="sxs-lookup"><span data-stu-id="89e79-126">System.String</span></span>

## <span data-ttu-id="89e79-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="89e79-127">OUTPUTS</span></span>

### <span data-ttu-id="89e79-128">Microsoft. Azure. Commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="89e79-128">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>
<span data-ttu-id="89e79-129">System. Collections. Generic. List \` 1 \[ \[ Microsoft. Azure. Commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule, Microsoft. Azure. Commands. IotHub, Version = 1.0.0.0, Culture = Neutral, PublicKeyToken = null\]\]</span><span class="sxs-lookup"><span data-stu-id="89e79-129">System.Collections.Generic.List\`1\[\[Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule, Microsoft.Azure.Commands.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null\]\]</span></span>

## <span data-ttu-id="89e79-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="89e79-130">NOTES</span></span>

## <span data-ttu-id="89e79-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="89e79-131">RELATED LINKS</span></span>

