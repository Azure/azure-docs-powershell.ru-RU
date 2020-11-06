---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/remove-azurermiothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubKey.md
ms.openlocfilehash: 4f1c21f4f64193ec25a0392e094b8fd492ceba9f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563484"
---
# <span data-ttu-id="f2a4d-101">Remove-AzureRmIotHubKey</span><span class="sxs-lookup"><span data-stu-id="f2a4d-101">Remove-AzureRmIotHubKey</span></span>

## <span data-ttu-id="f2a4d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f2a4d-102">SYNOPSIS</span></span>
<span data-ttu-id="f2a4d-103">Удаление IotHubого ключа.</span><span class="sxs-lookup"><span data-stu-id="f2a4d-103">Removes an IotHub Key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2a4d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f2a4d-104">SYNTAX</span></span>

```
Remove-AzureRmIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2a4d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f2a4d-105">DESCRIPTION</span></span>
<span data-ttu-id="f2a4d-106">Удаление IotHubого ключа.</span><span class="sxs-lookup"><span data-stu-id="f2a4d-106">Removes an IotHub Key.</span></span>
<span data-ttu-id="f2a4d-107">Если в списке есть несколько клавиш с одинаковым именем, первый из них будет удален.</span><span class="sxs-lookup"><span data-stu-id="f2a4d-107">If there are multiple keys with the same name the first one in the list is removed.</span></span>

## <span data-ttu-id="f2a4d-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f2a4d-108">EXAMPLES</span></span>

### <span data-ttu-id="f2a4d-109">Пример 1 удаление IotHub</span><span class="sxs-lookup"><span data-stu-id="f2a4d-109">Example 1 Delete an IotHub</span></span>
```
PS C:\> Remove-AzureRmIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner1"
```

<span data-ttu-id="f2a4d-110">Удаление ключа с именем iothubowner1 из IotHub с именем "myiothub"</span><span class="sxs-lookup"><span data-stu-id="f2a4d-110">Removes the key named iothubowner1 from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="f2a4d-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f2a4d-111">PARAMETERS</span></span>

### <span data-ttu-id="f2a4d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2a4d-112">-DefaultProfile</span></span>
<span data-ttu-id="f2a4d-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f2a4d-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f2a4d-114">-KeyName</span><span class="sxs-lookup"><span data-stu-id="f2a4d-114">-KeyName</span></span>
<span data-ttu-id="f2a4d-115">Имя ключа</span><span class="sxs-lookup"><span data-stu-id="f2a4d-115">Name of the Key</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2a4d-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f2a4d-116">-Name</span></span>
<span data-ttu-id="f2a4d-117">Имя IotHub</span><span class="sxs-lookup"><span data-stu-id="f2a4d-117">Name of the IotHub</span></span>

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

### <span data-ttu-id="f2a4d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2a4d-118">-ResourceGroupName</span></span>
<span data-ttu-id="f2a4d-119">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="f2a4d-119">Resource Group Name</span></span>

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

### <span data-ttu-id="f2a4d-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f2a4d-120">-Confirm</span></span>
<span data-ttu-id="f2a4d-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f2a4d-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2a4d-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2a4d-122">-WhatIf</span></span>
<span data-ttu-id="f2a4d-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f2a4d-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2a4d-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f2a4d-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2a4d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2a4d-125">CommonParameters</span></span>
<span data-ttu-id="f2a4d-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f2a4d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2a4d-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2a4d-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2a4d-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f2a4d-128">INPUTS</span></span>

### <span data-ttu-id="f2a4d-129">System. String</span><span class="sxs-lookup"><span data-stu-id="f2a4d-129">System.String</span></span>

## <span data-ttu-id="f2a4d-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f2a4d-130">OUTPUTS</span></span>

### <span data-ttu-id="f2a4d-131">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. IotHub... Models. PSSharedAccessSignatureAuthorizationRule, Microsoft. Azure. Commands. IotHub, Version = 1.0.0.0, Culture = "нейтрально", PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="f2a4d-131">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule, Microsoft.Azure.Commands.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="f2a4d-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="f2a4d-132">NOTES</span></span>

## <span data-ttu-id="f2a4d-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f2a4d-133">RELATED LINKS</span></span>

