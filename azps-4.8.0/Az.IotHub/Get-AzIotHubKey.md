---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubKey.md
ms.openlocfilehash: 258d1e1bad9eca1fd8817e1eaa499eb5bc3d8d49
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244921"
---
# <span data-ttu-id="0b952-101">Get-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="0b952-101">Get-AzIotHubKey</span></span>

## <span data-ttu-id="0b952-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0b952-102">SYNOPSIS</span></span>
<span data-ttu-id="0b952-103">Возвращает IotHub клавишу.</span><span class="sxs-lookup"><span data-stu-id="0b952-103">Gets an IotHub Key.</span></span>

## <span data-ttu-id="0b952-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0b952-104">SYNTAX</span></span>

### <span data-ttu-id="0b952-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0b952-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0b952-106">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="0b952-106">ResourceIdSet</span></span>
```
Get-AzIotHubKey [-HubId] <String> [[-KeyName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0b952-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0b952-107">DESCRIPTION</span></span>
<span data-ttu-id="0b952-108">Возвращает IotHub клавишу.</span><span class="sxs-lookup"><span data-stu-id="0b952-108">Gets an IotHub Key.</span></span>
<span data-ttu-id="0b952-109">Вы можете либо вывести список всех ключей, либо отфильтровать список по определенному названию ключа.</span><span class="sxs-lookup"><span data-stu-id="0b952-109">You can either list all Keys or filter the list by a specific Key Name.</span></span>

## <span data-ttu-id="0b952-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0b952-110">EXAMPLES</span></span>

### <span data-ttu-id="0b952-111">Пример 1 получить все клавиши</span><span class="sxs-lookup"><span data-stu-id="0b952-111">Example 1 Get all Keys</span></span>
```
PS C:\> Get-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="0b952-112">Возвращает все клавиши для IotHub с именем "myiothub"</span><span class="sxs-lookup"><span data-stu-id="0b952-112">Gets all the Keys for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="0b952-113">Пример 2 получение сведений о конкретном ключе</span><span class="sxs-lookup"><span data-stu-id="0b952-113">Example 2 Get information for a specific Key</span></span>
```
PS C:\> Get-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner"
```

<span data-ttu-id="0b952-114">Получает сведения для ключа с именем "iothubowner" для IotHub с именем "myiothub"</span><span class="sxs-lookup"><span data-stu-id="0b952-114">Gets the information for a key named "iothubowner" for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="0b952-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0b952-115">PARAMETERS</span></span>

### <span data-ttu-id="0b952-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b952-116">-DefaultProfile</span></span>
<span data-ttu-id="0b952-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="0b952-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0b952-118">-HubId</span><span class="sxs-lookup"><span data-stu-id="0b952-118">-HubId</span></span>
<span data-ttu-id="0b952-119">Идентификатор ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="0b952-119">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b952-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="0b952-120">-KeyName</span></span>
<span data-ttu-id="0b952-121">Имя ключа</span><span class="sxs-lookup"><span data-stu-id="0b952-121">Name of the Key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b952-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0b952-122">-Name</span></span>
<span data-ttu-id="0b952-123">Имя центра Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="0b952-123">Name of the IoT hub.</span></span> 

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b952-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b952-124">-ResourceGroupName</span></span>
<span data-ttu-id="0b952-125">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="0b952-125">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b952-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b952-126">CommonParameters</span></span>
<span data-ttu-id="0b952-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0b952-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b952-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b952-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b952-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0b952-129">INPUTS</span></span>

### <span data-ttu-id="0b952-130">System. String</span><span class="sxs-lookup"><span data-stu-id="0b952-130">System.String</span></span>

## <span data-ttu-id="0b952-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0b952-131">OUTPUTS</span></span>

### <span data-ttu-id="0b952-132">Microsoft. Azure. Commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="0b952-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="0b952-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="0b952-133">NOTES</span></span>

## <span data-ttu-id="0b952-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0b952-134">RELATED LINKS</span></span>