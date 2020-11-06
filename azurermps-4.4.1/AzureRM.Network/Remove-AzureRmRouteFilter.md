---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmRouteFilter.md
ms.openlocfilehash: 2d8bef14d13fb7b831312bb3dd7eb268c6c45b7b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563867"
---
# <span data-ttu-id="63252-101">Remove-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="63252-101">Remove-AzureRmRouteFilter</span></span>

## <span data-ttu-id="63252-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="63252-102">SYNOPSIS</span></span>
<span data-ttu-id="63252-103">{Заполнение кратких описаний}</span><span class="sxs-lookup"><span data-stu-id="63252-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="63252-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="63252-104">SYNTAX</span></span>

```
Remove-AzureRmRouteFilter -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63252-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="63252-105">DESCRIPTION</span></span>
<span data-ttu-id="63252-106">{Заполнение в описании}}</span><span class="sxs-lookup"><span data-stu-id="63252-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="63252-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="63252-107">EXAMPLES</span></span>

### <span data-ttu-id="63252-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="63252-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="63252-109">{{Добавить пример описания}}</span><span class="sxs-lookup"><span data-stu-id="63252-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="63252-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="63252-110">PARAMETERS</span></span>

### <span data-ttu-id="63252-111">-Force</span><span class="sxs-lookup"><span data-stu-id="63252-111">-Force</span></span>
<span data-ttu-id="63252-112">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="63252-112">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63252-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="63252-113">-Name</span></span>
<span data-ttu-id="63252-114">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="63252-114">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63252-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="63252-115">-PassThru</span></span>
<span data-ttu-id="63252-116">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="63252-116">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63252-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63252-117">-ResourceGroupName</span></span>
<span data-ttu-id="63252-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="63252-118">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63252-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="63252-119">-Confirm</span></span>
<span data-ttu-id="63252-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="63252-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63252-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63252-121">-WhatIf</span></span>
<span data-ttu-id="63252-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="63252-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63252-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="63252-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63252-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63252-124">-DefaultProfile</span></span>
<span data-ttu-id="63252-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="63252-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63252-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63252-126">CommonParameters</span></span>
<span data-ttu-id="63252-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="63252-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63252-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63252-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63252-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="63252-129">INPUTS</span></span>

### <span data-ttu-id="63252-130">System. String</span><span class="sxs-lookup"><span data-stu-id="63252-130">System.String</span></span>

## <span data-ttu-id="63252-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="63252-131">OUTPUTS</span></span>

### <span data-ttu-id="63252-132">System. Object</span><span class="sxs-lookup"><span data-stu-id="63252-132">System.Object</span></span>

## <span data-ttu-id="63252-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="63252-133">NOTES</span></span>

## <span data-ttu-id="63252-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="63252-134">RELATED LINKS</span></span>

