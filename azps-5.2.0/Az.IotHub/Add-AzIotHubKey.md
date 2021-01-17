---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubKey.md
ms.openlocfilehash: 422eb25456beb57ed6ab029fa5d70a47061ca491
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98399348"
---
# <span data-ttu-id="eefbc-101">Add-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="eefbc-101">Add-AzIotHubKey</span></span>

## <span data-ttu-id="eefbc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eefbc-102">SYNOPSIS</span></span>
<span data-ttu-id="eefbc-103">Создает ключ IotHub.</span><span class="sxs-lookup"><span data-stu-id="eefbc-103">Creates an IotHub Key.</span></span>

## <span data-ttu-id="eefbc-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="eefbc-104">SYNTAX</span></span>

### <span data-ttu-id="eefbc-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="eefbc-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String> [-PrimaryKey <String>]
 [-SecondaryKey <String>] -Rights <PSAccessRights> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eefbc-106">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="eefbc-106">ResourceIdSet</span></span>
```
Add-AzIotHubKey [-HubId] <String> [-KeyName] <String> [-PrimaryKey <String>] [-SecondaryKey <String>]
 -Rights <PSAccessRights> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eefbc-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eefbc-107">DESCRIPTION</span></span>
<span data-ttu-id="eefbc-108">Создает ключ для предоставленного IotHub.</span><span class="sxs-lookup"><span data-stu-id="eefbc-108">Creates a Key for the provided IotHub.</span></span>
<span data-ttu-id="eefbc-109">KeyNames не являются уникальными и требуют тщательного управление.</span><span class="sxs-lookup"><span data-stu-id="eefbc-109">KeyNames are not unique and need to be managed carefully.</span></span>

## <span data-ttu-id="eefbc-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="eefbc-110">EXAMPLES</span></span>

### <span data-ttu-id="eefbc-111">Пример 1. Добавление ключа в IotHub</span><span class="sxs-lookup"><span data-stu-id="eefbc-111">Example 1 Add a Key to an IotHub</span></span>
```
PS C:\> Add-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "newkey" -PrimaryKey "primarykey" -SecondaryKey "secondarykey" -Rights RegistryRead
```

<span data-ttu-id="eefbc-112">Создание ключа mykey для iothub "myiothub" с разрешениями RegistryRead.</span><span class="sxs-lookup"><span data-stu-id="eefbc-112">Creates a key named "mykey" for the iothub "myiothub" with RegistryRead permissions.</span></span>

## <span data-ttu-id="eefbc-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eefbc-113">PARAMETERS</span></span>

### <span data-ttu-id="eefbc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eefbc-114">-DefaultProfile</span></span>
<span data-ttu-id="eefbc-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="eefbc-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eefbc-116">-HubId</span><span class="sxs-lookup"><span data-stu-id="eefbc-116">-HubId</span></span>
<span data-ttu-id="eefbc-117">ИД ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="eefbc-117">IotHub Resource Id</span></span>

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

### <span data-ttu-id="eefbc-118">-KeyName</span><span class="sxs-lookup"><span data-stu-id="eefbc-118">-KeyName</span></span>
<span data-ttu-id="eefbc-119">Имя ключа</span><span class="sxs-lookup"><span data-stu-id="eefbc-119">Name of the Key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eefbc-120">-Name</span><span class="sxs-lookup"><span data-stu-id="eefbc-120">-Name</span></span>
<span data-ttu-id="eefbc-121">Имя IotHub</span><span class="sxs-lookup"><span data-stu-id="eefbc-121">Name of the IotHub</span></span>

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

### <span data-ttu-id="eefbc-122">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="eefbc-122">-PrimaryKey</span></span>
<span data-ttu-id="eefbc-123">Первичный ключ</span><span class="sxs-lookup"><span data-stu-id="eefbc-123">The primary key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eefbc-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eefbc-124">-ResourceGroupName</span></span>
<span data-ttu-id="eefbc-125">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="eefbc-125">Resource Group Name</span></span>

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

### <span data-ttu-id="eefbc-126">-Rights</span><span class="sxs-lookup"><span data-stu-id="eefbc-126">-Rights</span></span>
<span data-ttu-id="eefbc-127">Разрешения для этого IOTHub</span><span class="sxs-lookup"><span data-stu-id="eefbc-127">The permissions for this IOTHub</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSAccessRights
Parameter Sets: (All)
Aliases:
Accepted values: RegistryRead, RegistryWrite, ServiceConnect, DeviceConnect

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eefbc-128">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="eefbc-128">-SecondaryKey</span></span>
<span data-ttu-id="eefbc-129">Дополнительный ключ</span><span class="sxs-lookup"><span data-stu-id="eefbc-129">The Secondary Key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eefbc-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eefbc-130">-Confirm</span></span>
<span data-ttu-id="eefbc-131">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eefbc-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eefbc-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eefbc-132">-WhatIf</span></span>
<span data-ttu-id="eefbc-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eefbc-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eefbc-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="eefbc-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eefbc-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eefbc-135">CommonParameters</span></span>
<span data-ttu-id="eefbc-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eefbc-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eefbc-137">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eefbc-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eefbc-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="eefbc-138">INPUTS</span></span>

### <span data-ttu-id="eefbc-139">System.String</span><span class="sxs-lookup"><span data-stu-id="eefbc-139">System.String</span></span>

## <span data-ttu-id="eefbc-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="eefbc-140">OUTPUTS</span></span>

### <span data-ttu-id="eefbc-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="eefbc-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="eefbc-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="eefbc-142">NOTES</span></span>

## <span data-ttu-id="eefbc-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eefbc-143">RELATED LINKS</span></span>
