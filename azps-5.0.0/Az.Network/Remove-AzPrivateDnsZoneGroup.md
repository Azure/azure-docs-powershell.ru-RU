---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azprivatednszonegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateDnsZoneGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateDnsZoneGroup.md
ms.openlocfilehash: 1012bd4da163b992aec049643feb1e3fd8b4bf76
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94319145"
---
# <span data-ttu-id="04d61-101">Remove-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="04d61-101">Remove-AzPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="04d61-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="04d61-102">SYNOPSIS</span></span>
<span data-ttu-id="04d61-103">Удаляет группу зон DNS.</span><span class="sxs-lookup"><span data-stu-id="04d61-103">Removes a DNS zone group.</span></span>

## <span data-ttu-id="04d61-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="04d61-104">SYNTAX</span></span>

```
Remove-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String> -Name <String> [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04d61-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="04d61-105">DESCRIPTION</span></span>
<span data-ttu-id="04d61-106">Командлет **Remove-AzPrivateDnsZoneGroup** удаляет группу зон DNS.</span><span class="sxs-lookup"><span data-stu-id="04d61-106">The **Remove-AzPrivateDnsZoneGroup** cmdlet removes a DNS zone group.</span></span> 

## <span data-ttu-id="04d61-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="04d61-107">EXAMPLES</span></span>

### <span data-ttu-id="04d61-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="04d61-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzPrivateDnsZoneGroup -ResourceGroupName "rg" -PrivateEndpointName "test-pr-endpoint" -name dnsgroup1 
```

<span data-ttu-id="04d61-109">В приведенном выше примере удаляет зону DNS Grup с именем dnsgroup1 из конечной точки Test-PR-Endpoint.</span><span class="sxs-lookup"><span data-stu-id="04d61-109">Above example removes a DNS zone grup named dnsgroup1 from endpoint test-pr-endpoint.</span></span>

## <span data-ttu-id="04d61-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="04d61-110">PARAMETERS</span></span>

### <span data-ttu-id="04d61-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="04d61-111">-AsJob</span></span>
<span data-ttu-id="04d61-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="04d61-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="04d61-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04d61-113">-DefaultProfile</span></span>
<span data-ttu-id="04d61-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="04d61-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04d61-115">-Force</span><span class="sxs-lookup"><span data-stu-id="04d61-115">-Force</span></span>
<span data-ttu-id="04d61-116">Не запрашивать подтверждение, если вы хотите удалить ресурс</span><span class="sxs-lookup"><span data-stu-id="04d61-116">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="04d61-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="04d61-117">-Name</span></span>
<span data-ttu-id="04d61-118">Имя частной группы зоны DNS.</span><span class="sxs-lookup"><span data-stu-id="04d61-118">The name of the private dns zone group.</span></span>

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

### <span data-ttu-id="04d61-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="04d61-119">-PassThru</span></span>
<span data-ttu-id="04d61-120">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="04d61-120">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="04d61-121">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="04d61-121">-PrivateEndpointName</span></span>
<span data-ttu-id="04d61-122">Имя закрытой конечной точки.</span><span class="sxs-lookup"><span data-stu-id="04d61-122">The name of the private endpoint.</span></span>

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

### <span data-ttu-id="04d61-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04d61-123">-ResourceGroupName</span></span>
<span data-ttu-id="04d61-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="04d61-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="04d61-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="04d61-125">-Confirm</span></span>
<span data-ttu-id="04d61-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="04d61-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04d61-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04d61-127">-WhatIf</span></span>
<span data-ttu-id="04d61-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="04d61-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04d61-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="04d61-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04d61-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04d61-130">CommonParameters</span></span>
<span data-ttu-id="04d61-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="04d61-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04d61-132">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="04d61-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04d61-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="04d61-133">INPUTS</span></span>

### <span data-ttu-id="04d61-134">System. String</span><span class="sxs-lookup"><span data-stu-id="04d61-134">System.String</span></span>

## <span data-ttu-id="04d61-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="04d61-135">OUTPUTS</span></span>

### <span data-ttu-id="04d61-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="04d61-136">System.Boolean</span></span>

## <span data-ttu-id="04d61-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="04d61-137">NOTES</span></span>

## <span data-ttu-id="04d61-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="04d61-138">RELATED LINKS</span></span>
