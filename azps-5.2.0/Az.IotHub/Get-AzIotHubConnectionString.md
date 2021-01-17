---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConnectionString.md
ms.openlocfilehash: f84d233280bc771b90f47c5769fdb6d3f35c2e0c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98391127"
---
# <span data-ttu-id="19386-101">Get-AzIotHubConnectionString</span><span class="sxs-lookup"><span data-stu-id="19386-101">Get-AzIotHubConnectionString</span></span>

## <span data-ttu-id="19386-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19386-102">SYNOPSIS</span></span>
<span data-ttu-id="19386-103">Возвращает iotHub connectionstrings.</span><span class="sxs-lookup"><span data-stu-id="19386-103">Gets the IotHub connectionstrings.</span></span>

## <span data-ttu-id="19386-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="19386-104">SYNTAX</span></span>

```
Get-AzIotHubConnectionString [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19386-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="19386-105">DESCRIPTION</span></span>
<span data-ttu-id="19386-106">Возвращает iotHub connectionstrings.</span><span class="sxs-lookup"><span data-stu-id="19386-106">Gets the IotHub connectionstrings.</span></span>
<span data-ttu-id="19386-107">Вы можете получить подстроки для всех ключей или отфильтровать их по определенному имени ключа.</span><span class="sxs-lookup"><span data-stu-id="19386-107">You can either get connectionstrings for all the keys or filter them by a specific key name.</span></span>

## <span data-ttu-id="19386-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="19386-108">EXAMPLES</span></span>

### <span data-ttu-id="19386-109">Пример 1. Получить все iotHub connectionstrings</span><span class="sxs-lookup"><span data-stu-id="19386-109">Example 1 Get All IotHub connectionstrings</span></span>
```
PS C:\> Get-AzIotHubConnectionString -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="19386-110">Возвращает стрелки подключения для всех ключей iothub под названием "myiothub".</span><span class="sxs-lookup"><span data-stu-id="19386-110">Gets the connectionstrings for all keys for the iothub named "myiothub"</span></span>

### <span data-ttu-id="19386-111">Пример 2. Получить iotHub connectionstrings для определенного ключа</span><span class="sxs-lookup"><span data-stu-id="19386-111">Example 2 Get the IotHub connectionstrings for a specific key</span></span>
```
PS C:\> Get-AzIotHubConnectionString -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "mykey"
```

<span data-ttu-id="19386-112">Возвращает клавиши connectionstrings для ключа mykey для iothub под названием "myiothub".</span><span class="sxs-lookup"><span data-stu-id="19386-112">Gets the connectionstrings for the key named "mykey" for the iothub named "myiothub"</span></span>

## <span data-ttu-id="19386-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="19386-113">PARAMETERS</span></span>

### <span data-ttu-id="19386-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19386-114">-DefaultProfile</span></span>
<span data-ttu-id="19386-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="19386-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="19386-116">-KeyName</span><span class="sxs-lookup"><span data-stu-id="19386-116">-KeyName</span></span>
<span data-ttu-id="19386-117">Имя ключа</span><span class="sxs-lookup"><span data-stu-id="19386-117">Name of the Key</span></span>

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

### <span data-ttu-id="19386-118">-Name</span><span class="sxs-lookup"><span data-stu-id="19386-118">-Name</span></span>
<span data-ttu-id="19386-119">Имя IotHub</span><span class="sxs-lookup"><span data-stu-id="19386-119">Name of the IotHub</span></span>

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

### <span data-ttu-id="19386-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19386-120">-ResourceGroupName</span></span>
<span data-ttu-id="19386-121">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="19386-121">Resource Group Name</span></span>

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

### <span data-ttu-id="19386-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19386-122">CommonParameters</span></span>
<span data-ttu-id="19386-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19386-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19386-124">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19386-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19386-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="19386-125">INPUTS</span></span>

### <span data-ttu-id="19386-126">System.String</span><span class="sxs-lookup"><span data-stu-id="19386-126">System.String</span></span>

## <span data-ttu-id="19386-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="19386-127">OUTPUTS</span></span>

### <span data-ttu-id="19386-128">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="19386-128">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="19386-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="19386-129">NOTES</span></span>

## <span data-ttu-id="19386-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="19386-130">RELATED LINKS</span></span>
