---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubKey.md
ms.openlocfilehash: 258d1e1bad9eca1fd8817e1eaa499eb5bc3d8d49
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98409975"
---
# <span data-ttu-id="eea8d-101">Get-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="eea8d-101">Get-AzIotHubKey</span></span>

## <span data-ttu-id="eea8d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eea8d-102">SYNOPSIS</span></span>
<span data-ttu-id="eea8d-103">Возвращает ключ IotHub.</span><span class="sxs-lookup"><span data-stu-id="eea8d-103">Gets an IotHub Key.</span></span>

## <span data-ttu-id="eea8d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="eea8d-104">SYNTAX</span></span>

### <span data-ttu-id="eea8d-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="eea8d-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eea8d-106">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="eea8d-106">ResourceIdSet</span></span>
```
Get-AzIotHubKey [-HubId] <String> [[-KeyName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="eea8d-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eea8d-107">DESCRIPTION</span></span>
<span data-ttu-id="eea8d-108">Возвращает ключ IotHub.</span><span class="sxs-lookup"><span data-stu-id="eea8d-108">Gets an IotHub Key.</span></span>
<span data-ttu-id="eea8d-109">Вы можете перечислить все ключи или отфильтровать список по определенному имени ключа.</span><span class="sxs-lookup"><span data-stu-id="eea8d-109">You can either list all Keys or filter the list by a specific Key Name.</span></span>

## <span data-ttu-id="eea8d-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="eea8d-110">EXAMPLES</span></span>

### <span data-ttu-id="eea8d-111">Пример 1. Получить все ключи</span><span class="sxs-lookup"><span data-stu-id="eea8d-111">Example 1 Get all Keys</span></span>
```
PS C:\> Get-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="eea8d-112">Все клавиши для IotHub с именем "myiothub"</span><span class="sxs-lookup"><span data-stu-id="eea8d-112">Gets all the Keys for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="eea8d-113">Пример 2. Получить сведения для определенного ключа</span><span class="sxs-lookup"><span data-stu-id="eea8d-113">Example 2 Get information for a specific Key</span></span>
```
PS C:\> Get-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner"
```

<span data-ttu-id="eea8d-114">Возвращает сведения о ключе "iothubowner" для IotHub с именем Myiothub.</span><span class="sxs-lookup"><span data-stu-id="eea8d-114">Gets the information for a key named "iothubowner" for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="eea8d-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eea8d-115">PARAMETERS</span></span>

### <span data-ttu-id="eea8d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eea8d-116">-DefaultProfile</span></span>
<span data-ttu-id="eea8d-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="eea8d-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eea8d-118">-HubId</span><span class="sxs-lookup"><span data-stu-id="eea8d-118">-HubId</span></span>
<span data-ttu-id="eea8d-119">ИД ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="eea8d-119">IotHub Resource Id</span></span>

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

### <span data-ttu-id="eea8d-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="eea8d-120">-KeyName</span></span>
<span data-ttu-id="eea8d-121">Имя ключа</span><span class="sxs-lookup"><span data-stu-id="eea8d-121">Name of the Key</span></span>

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

### <span data-ttu-id="eea8d-122">-Name</span><span class="sxs-lookup"><span data-stu-id="eea8d-122">-Name</span></span>
<span data-ttu-id="eea8d-123">Имя концентратора IoT.</span><span class="sxs-lookup"><span data-stu-id="eea8d-123">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="eea8d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eea8d-124">-ResourceGroupName</span></span>
<span data-ttu-id="eea8d-125">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="eea8d-125">Resource Group Name</span></span>

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

### <span data-ttu-id="eea8d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eea8d-126">CommonParameters</span></span>
<span data-ttu-id="eea8d-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eea8d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eea8d-128">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eea8d-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eea8d-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="eea8d-129">INPUTS</span></span>

### <span data-ttu-id="eea8d-130">System.String</span><span class="sxs-lookup"><span data-stu-id="eea8d-130">System.String</span></span>

## <span data-ttu-id="eea8d-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="eea8d-131">OUTPUTS</span></span>

### <span data-ttu-id="eea8d-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="eea8d-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="eea8d-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="eea8d-133">NOTES</span></span>

## <span data-ttu-id="eea8d-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eea8d-134">RELATED LINKS</span></span>
