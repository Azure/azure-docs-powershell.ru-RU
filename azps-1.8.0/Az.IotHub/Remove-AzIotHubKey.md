---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubKey.md
ms.openlocfilehash: c275ac087c24c58de73e72ac5dcf46839d710621
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93900302"
---
# <span data-ttu-id="51bda-101">Remove-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="51bda-101">Remove-AzIotHubKey</span></span>

## <span data-ttu-id="51bda-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="51bda-102">SYNOPSIS</span></span>
<span data-ttu-id="51bda-103">Удаление IotHubого ключа.</span><span class="sxs-lookup"><span data-stu-id="51bda-103">Removes an IotHub Key.</span></span>

## <span data-ttu-id="51bda-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="51bda-104">SYNTAX</span></span>

```
Remove-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51bda-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="51bda-105">DESCRIPTION</span></span>
<span data-ttu-id="51bda-106">Удаление IotHubого ключа.</span><span class="sxs-lookup"><span data-stu-id="51bda-106">Removes an IotHub Key.</span></span>
<span data-ttu-id="51bda-107">Если в списке есть несколько клавиш с одинаковым именем, первый из них будет удален.</span><span class="sxs-lookup"><span data-stu-id="51bda-107">If there are multiple keys with the same name the first one in the list is removed.</span></span>

## <span data-ttu-id="51bda-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="51bda-108">EXAMPLES</span></span>

### <span data-ttu-id="51bda-109">Пример 1 удаление IotHub</span><span class="sxs-lookup"><span data-stu-id="51bda-109">Example 1 Delete an IotHub</span></span>
```
PS C:\> Remove-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner1"
```

<span data-ttu-id="51bda-110">Удаление ключа с именем iothubowner1 из IotHub с именем "myiothub"</span><span class="sxs-lookup"><span data-stu-id="51bda-110">Removes the key named iothubowner1 from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="51bda-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="51bda-111">PARAMETERS</span></span>

### <span data-ttu-id="51bda-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51bda-112">-DefaultProfile</span></span>
<span data-ttu-id="51bda-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="51bda-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="51bda-114">-KeyName</span><span class="sxs-lookup"><span data-stu-id="51bda-114">-KeyName</span></span>
<span data-ttu-id="51bda-115">Имя ключа</span><span class="sxs-lookup"><span data-stu-id="51bda-115">Name of the Key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51bda-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="51bda-116">-Name</span></span>
<span data-ttu-id="51bda-117">Имя IotHub</span><span class="sxs-lookup"><span data-stu-id="51bda-117">Name of the IotHub</span></span>

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

### <span data-ttu-id="51bda-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51bda-118">-ResourceGroupName</span></span>
<span data-ttu-id="51bda-119">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="51bda-119">Resource Group Name</span></span>

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

### <span data-ttu-id="51bda-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="51bda-120">-Confirm</span></span>
<span data-ttu-id="51bda-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="51bda-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51bda-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51bda-122">-WhatIf</span></span>
<span data-ttu-id="51bda-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="51bda-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51bda-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="51bda-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51bda-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51bda-125">CommonParameters</span></span>
<span data-ttu-id="51bda-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="51bda-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51bda-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51bda-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51bda-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="51bda-128">INPUTS</span></span>

### <span data-ttu-id="51bda-129">System. String</span><span class="sxs-lookup"><span data-stu-id="51bda-129">System.String</span></span>

## <span data-ttu-id="51bda-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="51bda-130">OUTPUTS</span></span>

### <span data-ttu-id="51bda-131">Microsoft. Azure. Commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="51bda-131">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="51bda-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="51bda-132">NOTES</span></span>

## <span data-ttu-id="51bda-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="51bda-133">RELATED LINKS</span></span>
