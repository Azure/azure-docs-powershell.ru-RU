---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubKey.md
ms.openlocfilehash: ac56d5392025a85d0310862a1786dde3d0f8ca2c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93900354"
---
# <span data-ttu-id="5f6b2-101">Get-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="5f6b2-101">Get-AzIotHubKey</span></span>

## <span data-ttu-id="5f6b2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5f6b2-102">SYNOPSIS</span></span>
<span data-ttu-id="5f6b2-103">Возвращает IotHub клавишу.</span><span class="sxs-lookup"><span data-stu-id="5f6b2-103">Gets an IotHub Key.</span></span>

## <span data-ttu-id="5f6b2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5f6b2-104">SYNTAX</span></span>

```
Get-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5f6b2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5f6b2-105">DESCRIPTION</span></span>
<span data-ttu-id="5f6b2-106">Возвращает IotHub клавишу.</span><span class="sxs-lookup"><span data-stu-id="5f6b2-106">Gets an IotHub Key.</span></span>
<span data-ttu-id="5f6b2-107">Вы можете либо вывести список всех ключей, либо отфильтровать список по определенному названию ключа.</span><span class="sxs-lookup"><span data-stu-id="5f6b2-107">You can either list all Keys or filter the list by a specific Key Name.</span></span>

## <span data-ttu-id="5f6b2-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5f6b2-108">EXAMPLES</span></span>

### <span data-ttu-id="5f6b2-109">Пример 1 получить все клавиши</span><span class="sxs-lookup"><span data-stu-id="5f6b2-109">Example 1 Get all Keys</span></span>
```
PS C:\> Get-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="5f6b2-110">Возвращает все клавиши для IotHub с именем "myiothub"</span><span class="sxs-lookup"><span data-stu-id="5f6b2-110">Gets all the Keys for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="5f6b2-111">Пример 2 получение сведений о конкретном ключе</span><span class="sxs-lookup"><span data-stu-id="5f6b2-111">Example 2 Get information for a specific Key</span></span>
```
PS C:\> Get-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner"
```

<span data-ttu-id="5f6b2-112">Получает сведения для ключа с именем "iothubowner" для IotHub с именем "myiothub"</span><span class="sxs-lookup"><span data-stu-id="5f6b2-112">Gets the information for a key named "iothubowner" for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="5f6b2-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5f6b2-113">PARAMETERS</span></span>

### <span data-ttu-id="5f6b2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f6b2-114">-DefaultProfile</span></span>
<span data-ttu-id="5f6b2-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="5f6b2-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5f6b2-116">-KeyName</span><span class="sxs-lookup"><span data-stu-id="5f6b2-116">-KeyName</span></span>
<span data-ttu-id="5f6b2-117">Имя ключа</span><span class="sxs-lookup"><span data-stu-id="5f6b2-117">Name of the Key</span></span>

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

### <span data-ttu-id="5f6b2-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5f6b2-118">-Name</span></span>
<span data-ttu-id="5f6b2-119">Имя центра Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="5f6b2-119">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="5f6b2-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f6b2-120">-ResourceGroupName</span></span>
<span data-ttu-id="5f6b2-121">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="5f6b2-121">Resource Group Name</span></span>

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

### <span data-ttu-id="5f6b2-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f6b2-122">CommonParameters</span></span>
<span data-ttu-id="5f6b2-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5f6b2-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f6b2-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f6b2-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f6b2-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5f6b2-125">INPUTS</span></span>

### <span data-ttu-id="5f6b2-126">System. String</span><span class="sxs-lookup"><span data-stu-id="5f6b2-126">System.String</span></span>

## <span data-ttu-id="5f6b2-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5f6b2-127">OUTPUTS</span></span>

### <span data-ttu-id="5f6b2-128">Microsoft. Azure. Commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="5f6b2-128">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="5f6b2-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="5f6b2-129">NOTES</span></span>

## <span data-ttu-id="5f6b2-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5f6b2-130">RELATED LINKS</span></span>
