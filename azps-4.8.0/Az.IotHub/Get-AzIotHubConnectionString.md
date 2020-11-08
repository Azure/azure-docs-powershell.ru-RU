---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConnectionString.md
ms.openlocfilehash: f84d233280bc771b90f47c5769fdb6d3f35c2e0c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079043"
---
# <span data-ttu-id="08e62-101">Get-AzIotHubConnectionString</span><span class="sxs-lookup"><span data-stu-id="08e62-101">Get-AzIotHubConnectionString</span></span>

## <span data-ttu-id="08e62-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="08e62-102">SYNOPSIS</span></span>
<span data-ttu-id="08e62-103">Возвращает IotHubные connectionStrings.</span><span class="sxs-lookup"><span data-stu-id="08e62-103">Gets the IotHub connectionstrings.</span></span>

## <span data-ttu-id="08e62-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="08e62-104">SYNTAX</span></span>

```
Get-AzIotHubConnectionString [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="08e62-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="08e62-105">DESCRIPTION</span></span>
<span data-ttu-id="08e62-106">Возвращает IotHubные connectionStrings.</span><span class="sxs-lookup"><span data-stu-id="08e62-106">Gets the IotHub connectionstrings.</span></span>
<span data-ttu-id="08e62-107">Вы можете либо получить ConnectionString для всех ключей, либо отфильтровать их по конкретному названию ключа.</span><span class="sxs-lookup"><span data-stu-id="08e62-107">You can either get connectionstrings for all the keys or filter them by a specific key name.</span></span>

## <span data-ttu-id="08e62-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="08e62-108">EXAMPLES</span></span>

### <span data-ttu-id="08e62-109">Пример 1 получение всех IotHub ConnectionString</span><span class="sxs-lookup"><span data-stu-id="08e62-109">Example 1 Get All IotHub connectionstrings</span></span>
```
PS C:\> Get-AzIotHubConnectionString -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="08e62-110">Получает префиксы ConnectionString для всех ключей для iothub с именем "myiothub"</span><span class="sxs-lookup"><span data-stu-id="08e62-110">Gets the connectionstrings for all keys for the iothub named "myiothub"</span></span>

### <span data-ttu-id="08e62-111">Пример 2. получение IotHub ConnectionString для определенного ключа</span><span class="sxs-lookup"><span data-stu-id="08e62-111">Example 2 Get the IotHub connectionstrings for a specific key</span></span>
```
PS C:\> Get-AzIotHubConnectionString -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "mykey"
```

<span data-ttu-id="08e62-112">Возвращает ConnectionString для ключа с именем "myKey" для iothub с именем "myiothub"</span><span class="sxs-lookup"><span data-stu-id="08e62-112">Gets the connectionstrings for the key named "mykey" for the iothub named "myiothub"</span></span>

## <span data-ttu-id="08e62-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="08e62-113">PARAMETERS</span></span>

### <span data-ttu-id="08e62-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08e62-114">-DefaultProfile</span></span>
<span data-ttu-id="08e62-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="08e62-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="08e62-116">-KeyName</span><span class="sxs-lookup"><span data-stu-id="08e62-116">-KeyName</span></span>
<span data-ttu-id="08e62-117">Имя ключа</span><span class="sxs-lookup"><span data-stu-id="08e62-117">Name of the Key</span></span>

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

### <span data-ttu-id="08e62-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="08e62-118">-Name</span></span>
<span data-ttu-id="08e62-119">Имя IotHub</span><span class="sxs-lookup"><span data-stu-id="08e62-119">Name of the IotHub</span></span>

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

### <span data-ttu-id="08e62-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08e62-120">-ResourceGroupName</span></span>
<span data-ttu-id="08e62-121">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="08e62-121">Resource Group Name</span></span>

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

### <span data-ttu-id="08e62-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08e62-122">CommonParameters</span></span>
<span data-ttu-id="08e62-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="08e62-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08e62-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08e62-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08e62-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="08e62-125">INPUTS</span></span>

### <span data-ttu-id="08e62-126">System. String</span><span class="sxs-lookup"><span data-stu-id="08e62-126">System.String</span></span>

## <span data-ttu-id="08e62-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="08e62-127">OUTPUTS</span></span>

### <span data-ttu-id="08e62-128">Microsoft. Azure. Commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="08e62-128">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="08e62-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="08e62-129">NOTES</span></span>

## <span data-ttu-id="08e62-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="08e62-130">RELATED LINKS</span></span>
