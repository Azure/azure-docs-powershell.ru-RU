---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubKey.md
ms.openlocfilehash: c50ee56a5dcb15c3b199e9aaf08aeca74828cc66
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079992"
---
# <span data-ttu-id="0ff9c-101">Remove-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="0ff9c-101">Remove-AzIotHubKey</span></span>

## <span data-ttu-id="0ff9c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0ff9c-102">SYNOPSIS</span></span>
<span data-ttu-id="0ff9c-103">Удаление IotHubого ключа.</span><span class="sxs-lookup"><span data-stu-id="0ff9c-103">Removes an IotHub Key.</span></span>

## <span data-ttu-id="0ff9c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0ff9c-104">SYNTAX</span></span>

### <span data-ttu-id="0ff9c-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0ff9c-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ff9c-106">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="0ff9c-106">ResourceIdSet</span></span>
```
Remove-AzIotHubKey [-HubId] <String> [-KeyName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ff9c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0ff9c-107">DESCRIPTION</span></span>
<span data-ttu-id="0ff9c-108">Удаление IotHubого ключа.</span><span class="sxs-lookup"><span data-stu-id="0ff9c-108">Removes an IotHub Key.</span></span>
<span data-ttu-id="0ff9c-109">Если в списке есть несколько клавиш с одинаковым именем, первый из них будет удален.</span><span class="sxs-lookup"><span data-stu-id="0ff9c-109">If there are multiple keys with the same name the first one in the list is removed.</span></span>

## <span data-ttu-id="0ff9c-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0ff9c-110">EXAMPLES</span></span>

### <span data-ttu-id="0ff9c-111">Пример 1 удаление IotHub</span><span class="sxs-lookup"><span data-stu-id="0ff9c-111">Example 1 Delete an IotHub</span></span>
```
PS C:\> Remove-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner1"
```

<span data-ttu-id="0ff9c-112">Удаление ключа с именем iothubowner1 из IotHub с именем "myiothub"</span><span class="sxs-lookup"><span data-stu-id="0ff9c-112">Removes the key named iothubowner1 from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="0ff9c-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0ff9c-113">PARAMETERS</span></span>

### <span data-ttu-id="0ff9c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ff9c-114">-DefaultProfile</span></span>
<span data-ttu-id="0ff9c-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="0ff9c-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0ff9c-116">-HubId</span><span class="sxs-lookup"><span data-stu-id="0ff9c-116">-HubId</span></span>
<span data-ttu-id="0ff9c-117">Идентификатор ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="0ff9c-117">IotHub Resource Id</span></span>

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

### <span data-ttu-id="0ff9c-118">-KeyName</span><span class="sxs-lookup"><span data-stu-id="0ff9c-118">-KeyName</span></span>
<span data-ttu-id="0ff9c-119">Имя ключа</span><span class="sxs-lookup"><span data-stu-id="0ff9c-119">Name of the Key</span></span>

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

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ff9c-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0ff9c-120">-Name</span></span>
<span data-ttu-id="0ff9c-121">Имя IotHub</span><span class="sxs-lookup"><span data-stu-id="0ff9c-121">Name of the IotHub</span></span>

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

### <span data-ttu-id="0ff9c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ff9c-122">-ResourceGroupName</span></span>
<span data-ttu-id="0ff9c-123">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="0ff9c-123">Resource Group Name</span></span>

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

### <span data-ttu-id="0ff9c-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0ff9c-124">-Confirm</span></span>
<span data-ttu-id="0ff9c-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0ff9c-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ff9c-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ff9c-126">-WhatIf</span></span>
<span data-ttu-id="0ff9c-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0ff9c-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ff9c-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0ff9c-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ff9c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ff9c-129">CommonParameters</span></span>
<span data-ttu-id="0ff9c-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0ff9c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ff9c-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ff9c-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ff9c-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0ff9c-132">INPUTS</span></span>

### <span data-ttu-id="0ff9c-133">System. String</span><span class="sxs-lookup"><span data-stu-id="0ff9c-133">System.String</span></span>

## <span data-ttu-id="0ff9c-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0ff9c-134">OUTPUTS</span></span>

### <span data-ttu-id="0ff9c-135">Microsoft. Azure. Commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="0ff9c-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="0ff9c-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="0ff9c-136">NOTES</span></span>

## <span data-ttu-id="0ff9c-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0ff9c-137">RELATED LINKS</span></span>
