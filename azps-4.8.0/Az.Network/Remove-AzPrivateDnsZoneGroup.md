---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azprivatednszonegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateDnsZoneGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateDnsZoneGroup.md
ms.openlocfilehash: 1012bd4da163b992aec049643feb1e3fd8b4bf76
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94234912"
---
# <span data-ttu-id="b4633-101">Remove-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="b4633-101">Remove-AzPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="b4633-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b4633-102">SYNOPSIS</span></span>
<span data-ttu-id="b4633-103">Удаляет группу зон DNS.</span><span class="sxs-lookup"><span data-stu-id="b4633-103">Removes a DNS zone group.</span></span>

## <span data-ttu-id="b4633-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b4633-104">SYNTAX</span></span>

```
Remove-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String> -Name <String> [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4633-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b4633-105">DESCRIPTION</span></span>
<span data-ttu-id="b4633-106">Командлет **Remove-AzPrivateDnsZoneGroup** удаляет группу зон DNS.</span><span class="sxs-lookup"><span data-stu-id="b4633-106">The **Remove-AzPrivateDnsZoneGroup** cmdlet removes a DNS zone group.</span></span> 

## <span data-ttu-id="b4633-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b4633-107">EXAMPLES</span></span>

### <span data-ttu-id="b4633-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b4633-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzPrivateDnsZoneGroup -ResourceGroupName "rg" -PrivateEndpointName "test-pr-endpoint" -name dnsgroup1 
```

<span data-ttu-id="b4633-109">В приведенном выше примере удаляет зону DNS Grup с именем dnsgroup1 из конечной точки Test-PR-Endpoint.</span><span class="sxs-lookup"><span data-stu-id="b4633-109">Above example removes a DNS zone grup named dnsgroup1 from endpoint test-pr-endpoint.</span></span>

## <span data-ttu-id="b4633-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b4633-110">PARAMETERS</span></span>

### <span data-ttu-id="b4633-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b4633-111">-AsJob</span></span>
<span data-ttu-id="b4633-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="b4633-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b4633-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4633-113">-DefaultProfile</span></span>
<span data-ttu-id="b4633-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b4633-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4633-115">-Force</span><span class="sxs-lookup"><span data-stu-id="b4633-115">-Force</span></span>
<span data-ttu-id="b4633-116">Не запрашивать подтверждение, если вы хотите удалить ресурс</span><span class="sxs-lookup"><span data-stu-id="b4633-116">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="b4633-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b4633-117">-Name</span></span>
<span data-ttu-id="b4633-118">Имя частной группы зоны DNS.</span><span class="sxs-lookup"><span data-stu-id="b4633-118">The name of the private dns zone group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PrivateDnsZoneGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4633-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b4633-119">-PassThru</span></span>
<span data-ttu-id="b4633-120">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="b4633-120">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="b4633-121">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="b4633-121">-PrivateEndpointName</span></span>
<span data-ttu-id="b4633-122">Имя закрытой конечной точки.</span><span class="sxs-lookup"><span data-stu-id="b4633-122">The name of the private endpoint.</span></span>

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

### <span data-ttu-id="b4633-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4633-123">-ResourceGroupName</span></span>
<span data-ttu-id="b4633-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b4633-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="b4633-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b4633-125">-Confirm</span></span>
<span data-ttu-id="b4633-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b4633-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4633-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4633-127">-WhatIf</span></span>
<span data-ttu-id="b4633-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b4633-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4633-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b4633-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4633-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4633-130">CommonParameters</span></span>
<span data-ttu-id="b4633-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b4633-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4633-132">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b4633-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4633-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b4633-133">INPUTS</span></span>

### <span data-ttu-id="b4633-134">System. String</span><span class="sxs-lookup"><span data-stu-id="b4633-134">System.String</span></span>

## <span data-ttu-id="b4633-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b4633-135">OUTPUTS</span></span>

### <span data-ttu-id="b4633-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b4633-136">System.Boolean</span></span>

## <span data-ttu-id="b4633-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="b4633-137">NOTES</span></span>

## <span data-ttu-id="b4633-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b4633-138">RELATED LINKS</span></span>
