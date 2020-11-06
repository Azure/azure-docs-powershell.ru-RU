---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubConnectionString.md
ms.openlocfilehash: ef4ac5058c1ce85e19a9854bcd11fc2fac5ac69e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564879"
---
# <span data-ttu-id="50941-101">Get-AzureRmIotHubConnectionString</span><span class="sxs-lookup"><span data-stu-id="50941-101">Get-AzureRmIotHubConnectionString</span></span>

## <span data-ttu-id="50941-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="50941-102">SYNOPSIS</span></span>
<span data-ttu-id="50941-103">Возвращает IotHubные connectionStrings.</span><span class="sxs-lookup"><span data-stu-id="50941-103">Gets the IotHub connectionstrings.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="50941-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="50941-104">SYNTAX</span></span>

```
Get-AzureRmIotHubConnectionString [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="50941-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="50941-105">DESCRIPTION</span></span>
<span data-ttu-id="50941-106">Возвращает IotHubные connectionStrings.</span><span class="sxs-lookup"><span data-stu-id="50941-106">Gets the IotHub connectionstrings.</span></span>
<span data-ttu-id="50941-107">Вы можете либо получить ConnectionString для всех ключей, либо отфильтровать их по конкретному названию ключа.</span><span class="sxs-lookup"><span data-stu-id="50941-107">You can either get connectionstrings for all the keys or filter them by a specific key name.</span></span>

## <span data-ttu-id="50941-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="50941-108">EXAMPLES</span></span>

### <span data-ttu-id="50941-109">Пример 1 получение всех IotHub ConnectionString</span><span class="sxs-lookup"><span data-stu-id="50941-109">Example 1 Get All IotHub connectionstrings</span></span>
```
PS C:\> Get-AzureRmIotHubConnectionString -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="50941-110">Получает префиксы ConnectionString для всех ключей для iothub с именем "myiothub"</span><span class="sxs-lookup"><span data-stu-id="50941-110">Gets the connectionstrings for all keys for the iothub named "myiothub"</span></span>

### <span data-ttu-id="50941-111">Пример 2. получение IotHub ConnectionString для определенного ключа</span><span class="sxs-lookup"><span data-stu-id="50941-111">Example 2 Get the IotHub connectionstrings for a specific key</span></span>
```
PS C:\> Get-AzureRmIotHubConnectionString -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "mykey"
```

<span data-ttu-id="50941-112">Возвращает ConnectionString для ключа с именем "myKey" для iothub с именем "myiothub"</span><span class="sxs-lookup"><span data-stu-id="50941-112">Gets the connectionstrings for the key named "mykey" for the iothub named "myiothub"</span></span>

## <span data-ttu-id="50941-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="50941-113">PARAMETERS</span></span>

### <span data-ttu-id="50941-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50941-114">-DefaultProfile</span></span>
<span data-ttu-id="50941-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="50941-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="50941-116">-KeyName</span><span class="sxs-lookup"><span data-stu-id="50941-116">-KeyName</span></span>
<span data-ttu-id="50941-117">Имя ключа</span><span class="sxs-lookup"><span data-stu-id="50941-117">Name of the Key</span></span>

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

### <span data-ttu-id="50941-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="50941-118">-Name</span></span>
<span data-ttu-id="50941-119">Имя IotHub</span><span class="sxs-lookup"><span data-stu-id="50941-119">Name of the IotHub</span></span>

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

### <span data-ttu-id="50941-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50941-120">-ResourceGroupName</span></span>
<span data-ttu-id="50941-121">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="50941-121">Resource Group Name</span></span>

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

### <span data-ttu-id="50941-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50941-122">CommonParameters</span></span>
<span data-ttu-id="50941-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="50941-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50941-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50941-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50941-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="50941-125">INPUTS</span></span>

### <span data-ttu-id="50941-126">System. String</span><span class="sxs-lookup"><span data-stu-id="50941-126">System.String</span></span>

## <span data-ttu-id="50941-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="50941-127">OUTPUTS</span></span>

### <span data-ttu-id="50941-128">Microsoft. Azure. Commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="50941-128">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>
<span data-ttu-id="50941-129">System. Collections. Generic. List \` 1 \[ \[ Microsoft. Azure. Commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule, Microsoft. Azure. Commands. IotHub, Version = 1.0.0.0, Culture = Neutral, PublicKeyToken = null\]\]</span><span class="sxs-lookup"><span data-stu-id="50941-129">System.Collections.Generic.List\`1\[\[Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule, Microsoft.Azure.Commands.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null\]\]</span></span>

## <span data-ttu-id="50941-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="50941-130">NOTES</span></span>

## <span data-ttu-id="50941-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="50941-131">RELATED LINKS</span></span>

