---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubKey.md
ms.openlocfilehash: db2cf6c9daae5b96642a6408b990276feffc8598
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567618"
---
# <span data-ttu-id="3754f-101">Get-AzureRmIotHubKey</span><span class="sxs-lookup"><span data-stu-id="3754f-101">Get-AzureRmIotHubKey</span></span>

## <span data-ttu-id="3754f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3754f-102">SYNOPSIS</span></span>
<span data-ttu-id="3754f-103">Возвращает IotHub клавишу.</span><span class="sxs-lookup"><span data-stu-id="3754f-103">Gets an IotHub Key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3754f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3754f-104">SYNTAX</span></span>

```
Get-AzureRmIotHubKey [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3754f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3754f-105">DESCRIPTION</span></span>
<span data-ttu-id="3754f-106">Возвращает IotHub клавишу.</span><span class="sxs-lookup"><span data-stu-id="3754f-106">Gets an IotHub Key.</span></span>
<span data-ttu-id="3754f-107">Вы можете либо вывести список всех ключей, либо отфильтровать список по определенному названию ключа.</span><span class="sxs-lookup"><span data-stu-id="3754f-107">You can either list all Keys or filter the list by a specific Key Name.</span></span>

## <span data-ttu-id="3754f-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3754f-108">EXAMPLES</span></span>

### <span data-ttu-id="3754f-109">Пример 1 получить все клавиши</span><span class="sxs-lookup"><span data-stu-id="3754f-109">Example 1 Get all Keys</span></span>
```
PS C:\> Get-AzureRmIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="3754f-110">Возвращает все клавиши для IotHub с именем "myiothub"</span><span class="sxs-lookup"><span data-stu-id="3754f-110">Gets all the Keys for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="3754f-111">Пример 2 получение сведений о конкретном ключе</span><span class="sxs-lookup"><span data-stu-id="3754f-111">Example 2 Get information for a specific Key</span></span>
```
PS C:\> Get-AzureRmIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner"
```

<span data-ttu-id="3754f-112">Получает сведения для ключа с именем "iothubowner" для IotHub с именем "myiothub"</span><span class="sxs-lookup"><span data-stu-id="3754f-112">Gets the information for a key named "iothubowner" for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="3754f-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3754f-113">PARAMETERS</span></span>

### <span data-ttu-id="3754f-114">-KeyName</span><span class="sxs-lookup"><span data-stu-id="3754f-114">-KeyName</span></span>
<span data-ttu-id="3754f-115">Имя ключа</span><span class="sxs-lookup"><span data-stu-id="3754f-115">Name of the Key</span></span>

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

### <span data-ttu-id="3754f-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3754f-116">-Name</span></span>
<span data-ttu-id="3754f-117">Имя центра Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="3754f-117">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="3754f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3754f-118">-ResourceGroupName</span></span>
<span data-ttu-id="3754f-119">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="3754f-119">Resource Group Name</span></span>

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

### <span data-ttu-id="3754f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3754f-120">-DefaultProfile</span></span>
<span data-ttu-id="3754f-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3754f-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3754f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3754f-122">CommonParameters</span></span>
<span data-ttu-id="3754f-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3754f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3754f-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3754f-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3754f-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3754f-125">INPUTS</span></span>

### <span data-ttu-id="3754f-126">System. String</span><span class="sxs-lookup"><span data-stu-id="3754f-126">System.String</span></span>

## <span data-ttu-id="3754f-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3754f-127">OUTPUTS</span></span>

### <span data-ttu-id="3754f-128">Microsoft. Azure. Commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="3754f-128">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>
<span data-ttu-id="3754f-129">System. Collections. Generic. List \` 1 \[ \[ Microsoft. Azure. Commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule, Microsoft. Azure. Commands. IotHub, Version = 1.0.0.0, Culture = Neutral, PublicKeyToken = null\]\]</span><span class="sxs-lookup"><span data-stu-id="3754f-129">System.Collections.Generic.List\`1\[\[Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule, Microsoft.Azure.Commands.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null\]\]</span></span>

## <span data-ttu-id="3754f-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="3754f-130">NOTES</span></span>

## <span data-ttu-id="3754f-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3754f-131">RELATED LINKS</span></span>

