---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConnectionString.md
ms.openlocfilehash: f89d47dac0b48ca82b2478743d2993f94fb792d1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720754"
---
# <span data-ttu-id="704c8-101">Get-AzIotHubConnectionString</span><span class="sxs-lookup"><span data-stu-id="704c8-101">Get-AzIotHubConnectionString</span></span>

## <span data-ttu-id="704c8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="704c8-102">SYNOPSIS</span></span>
<span data-ttu-id="704c8-103">Возвращает IotHubные connectionStrings.</span><span class="sxs-lookup"><span data-stu-id="704c8-103">Gets the IotHub connectionstrings.</span></span>

## <span data-ttu-id="704c8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="704c8-104">SYNTAX</span></span>

```
Get-AzIotHubConnectionString [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="704c8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="704c8-105">DESCRIPTION</span></span>
<span data-ttu-id="704c8-106">Возвращает IotHubные connectionStrings.</span><span class="sxs-lookup"><span data-stu-id="704c8-106">Gets the IotHub connectionstrings.</span></span>
<span data-ttu-id="704c8-107">Вы можете либо получить ConnectionString для всех ключей, либо отфильтровать их по конкретному названию ключа.</span><span class="sxs-lookup"><span data-stu-id="704c8-107">You can either get connectionstrings for all the keys or filter them by a specific key name.</span></span>

## <span data-ttu-id="704c8-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="704c8-108">EXAMPLES</span></span>

### <span data-ttu-id="704c8-109">Пример 1 получение всех IotHub ConnectionString</span><span class="sxs-lookup"><span data-stu-id="704c8-109">Example 1 Get All IotHub connectionstrings</span></span>
```
PS C:\> Get-AzIotHubConnectionString -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="704c8-110">Получает префиксы ConnectionString для всех ключей для iothub с именем "myiothub"</span><span class="sxs-lookup"><span data-stu-id="704c8-110">Gets the connectionstrings for all keys for the iothub named "myiothub"</span></span>

### <span data-ttu-id="704c8-111">Пример 2. получение IotHub ConnectionString для определенного ключа</span><span class="sxs-lookup"><span data-stu-id="704c8-111">Example 2 Get the IotHub connectionstrings for a specific key</span></span>
```
PS C:\> Get-AzIotHubConnectionString -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "mykey"
```

<span data-ttu-id="704c8-112">Возвращает ConnectionString для ключа с именем "myKey" для iothub с именем "myiothub"</span><span class="sxs-lookup"><span data-stu-id="704c8-112">Gets the connectionstrings for the key named "mykey" for the iothub named "myiothub"</span></span>

## <span data-ttu-id="704c8-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="704c8-113">PARAMETERS</span></span>

### <span data-ttu-id="704c8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="704c8-114">-DefaultProfile</span></span>
<span data-ttu-id="704c8-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="704c8-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="704c8-116">-KeyName</span><span class="sxs-lookup"><span data-stu-id="704c8-116">-KeyName</span></span>
<span data-ttu-id="704c8-117">Имя ключа</span><span class="sxs-lookup"><span data-stu-id="704c8-117">Name of the Key</span></span>

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

### <span data-ttu-id="704c8-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="704c8-118">-Name</span></span>
<span data-ttu-id="704c8-119">Имя IotHub</span><span class="sxs-lookup"><span data-stu-id="704c8-119">Name of the IotHub</span></span>

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

### <span data-ttu-id="704c8-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="704c8-120">-ResourceGroupName</span></span>
<span data-ttu-id="704c8-121">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="704c8-121">Resource Group Name</span></span>

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

### <span data-ttu-id="704c8-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="704c8-122">CommonParameters</span></span>
<span data-ttu-id="704c8-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="704c8-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="704c8-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="704c8-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="704c8-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="704c8-125">INPUTS</span></span>

### <span data-ttu-id="704c8-126">System. String</span><span class="sxs-lookup"><span data-stu-id="704c8-126">System.String</span></span>

## <span data-ttu-id="704c8-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="704c8-127">OUTPUTS</span></span>

### <span data-ttu-id="704c8-128">Microsoft. Azure. Commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="704c8-128">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="704c8-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="704c8-129">NOTES</span></span>

## <span data-ttu-id="704c8-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="704c8-130">RELATED LINKS</span></span>
