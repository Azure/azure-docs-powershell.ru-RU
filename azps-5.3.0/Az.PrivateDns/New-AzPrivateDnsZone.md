---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/new-azprivatednszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsZone.md
ms.openlocfilehash: 98830e2dbcfc115cd026c33782030bc40fa6763f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98420303"
---
# <span data-ttu-id="5c309-101">New-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="5c309-101">New-AzPrivateDnsZone</span></span>

## <span data-ttu-id="5c309-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c309-102">SYNOPSIS</span></span>
<span data-ttu-id="5c309-103">Создает новую частную зону DNS.</span><span class="sxs-lookup"><span data-stu-id="5c309-103">Creates a new private DNS zone.</span></span>

## <span data-ttu-id="5c309-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5c309-104">SYNTAX</span></span>

```
New-AzPrivateDnsZone -ResourceGroupName <String> -Name <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c309-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5c309-105">DESCRIPTION</span></span>
<span data-ttu-id="5c309-106">Для создания новой зоны частного доменного имени (DNS) в указанной группе ресурсов будет указана новая зона **AzPrivateDnsZone.**</span><span class="sxs-lookup"><span data-stu-id="5c309-106">The **New-AzPrivateDnsZone** cmdlet creates a new private Domain Name System (DNS) zone in the specified resource group.</span></span> <span data-ttu-id="5c309-107">Необходимо указать уникальное имя зоны DNS для параметра *Name,* иначе при этом будет возвращена ошибка.</span><span class="sxs-lookup"><span data-stu-id="5c309-107">You must specify a unique private DNS zone name for the *Name* parameter or the cmdlet will return an error.</span></span> <span data-ttu-id="5c309-108">После создания зоны создайте в New-AzPrivateDnsRecordSet наборы записей с помощью New-AzPrivateDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="5c309-108">After the zone is created, use the New-AzPrivateDnsRecordSet cmdlet to create record sets in the zone.</span></span>
<span data-ttu-id="5c309-109">С помощью переменных *Confirm* и $ConfirmPreference Windows PowerShell можно управлять запросом на подтверждение с помощью cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5c309-109">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="5c309-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5c309-110">EXAMPLES</span></span>

### <span data-ttu-id="5c309-111">Пример 1. Создание частной зоны DNS</span><span class="sxs-lookup"><span data-stu-id="5c309-111">Example 1: Create a Private DNS zone</span></span>
```
PS C:\>$Zone = New-AzPrivateDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"


This command creates a new private DNS zone named myzone.com in the specified resource group, and then
stores it in the $Zone variable. $Zone object looks something like this,

Name                          : myzone.com
ResourceId                    : "/subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/PrivateZones/myzone.com"
ResourceGroupName             : MyResourceGroup
Location                      : 
Etag                          : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags                          : {}
NumberOfRecordSets            : 1
MaxNumberOfRecordSets         : 5000
```

## <span data-ttu-id="5c309-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5c309-112">PARAMETERS</span></span>

### <span data-ttu-id="5c309-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c309-113">-DefaultProfile</span></span>
<span data-ttu-id="5c309-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="5c309-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5c309-115">-Name</span><span class="sxs-lookup"><span data-stu-id="5c309-115">-Name</span></span>
<span data-ttu-id="5c309-116">Указывает имя частного DNS-зоны, который нужно создать.</span><span class="sxs-lookup"><span data-stu-id="5c309-116">Specifies the name of the private DNS zone to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c309-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c309-117">-ResourceGroupName</span></span>
<span data-ttu-id="5c309-118">Определяет группу ресурсов, в которой нужно создать зону.</span><span class="sxs-lookup"><span data-stu-id="5c309-118">Specifies the resource group in which to create the zone.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c309-119">-Tag</span><span class="sxs-lookup"><span data-stu-id="5c309-119">-Tag</span></span>
<span data-ttu-id="5c309-120">Hash table which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="5c309-120">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c309-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5c309-121">-Confirm</span></span>
<span data-ttu-id="5c309-122">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="5c309-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c309-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c309-123">-WhatIf</span></span>
<span data-ttu-id="5c309-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5c309-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5c309-125">Этот cmdlet не будет выполниться. Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5c309-125">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5c309-126">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="5c309-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c309-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c309-127">CommonParameters</span></span>
<span data-ttu-id="5c309-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c309-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c309-129">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c309-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c309-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5c309-130">INPUTS</span></span>

### <span data-ttu-id="5c309-131">Нет</span><span class="sxs-lookup"><span data-stu-id="5c309-131">None</span></span>

## <span data-ttu-id="5c309-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5c309-132">OUTPUTS</span></span>

### <span data-ttu-id="5c309-133">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="5c309-133">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

## <span data-ttu-id="5c309-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5c309-134">NOTES</span></span>

## <span data-ttu-id="5c309-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5c309-135">RELATED LINKS</span></span>

[<span data-ttu-id="5c309-136">Get-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="5c309-136">Get-AzPrivateDnsZone</span></span>](./Get-AzPrivateDnsZone.md)

[<span data-ttu-id="5c309-137">New-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="5c309-137">New-AzPrivateDnsRecordSet</span></span>](./New-AzPrivateDnsRecordSet.md)

[<span data-ttu-id="5c309-138">Remove-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="5c309-138">Remove-AzPrivateDnsZone</span></span>](./Remove-AzPrivateDnsZone.md)
