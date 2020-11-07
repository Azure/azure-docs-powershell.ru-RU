---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/new-azprivatednszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsZone.md
ms.openlocfilehash: 20922936f754f18d2ee26631dc616d9723cdc5e5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729782"
---
# <span data-ttu-id="cc970-101">New-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="cc970-101">New-AzPrivateDnsZone</span></span>

## <span data-ttu-id="cc970-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cc970-102">SYNOPSIS</span></span>
<span data-ttu-id="cc970-103">Создание частной зоны DNS.</span><span class="sxs-lookup"><span data-stu-id="cc970-103">Creates a new private DNS zone.</span></span>

## <span data-ttu-id="cc970-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cc970-104">SYNTAX</span></span>

```
New-AzPrivateDnsZone -ResourceGroupName <String> -Name <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc970-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cc970-105">DESCRIPTION</span></span>
<span data-ttu-id="cc970-106">Командлет **New-AzPrivateDnsZone** создает новую зону DNS (Private Domain Name System) в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cc970-106">The **New-AzPrivateDnsZone** cmdlet creates a new private Domain Name System (DNS) zone in the specified resource group.</span></span> <span data-ttu-id="cc970-107">Для параметра *Name* необходимо указать уникальное имя частной зоны DNS или командлет будет возвращать ошибку.</span><span class="sxs-lookup"><span data-stu-id="cc970-107">You must specify a unique private DNS zone name for the *Name* parameter or the cmdlet will return an error.</span></span> <span data-ttu-id="cc970-108">После создания зоны используйте командлет New-AzPrivateDnsRecordSet для создания наборов записей в зоне.</span><span class="sxs-lookup"><span data-stu-id="cc970-108">After the zone is created, use the New-AzPrivateDnsRecordSet cmdlet to create record sets in the zone.</span></span>
<span data-ttu-id="cc970-109">Вы можете использовать параметр *Confirm* и $ConfirmPreference переменной Windows PowerShell, чтобы указать, нужно ли командлету запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="cc970-109">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="cc970-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cc970-110">EXAMPLES</span></span>

### <span data-ttu-id="cc970-111">Пример 1: создание частной зоны DNS</span><span class="sxs-lookup"><span data-stu-id="cc970-111">Example 1: Create a Private DNS zone</span></span>
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

## <span data-ttu-id="cc970-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cc970-112">PARAMETERS</span></span>

### <span data-ttu-id="cc970-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc970-113">-DefaultProfile</span></span>
<span data-ttu-id="cc970-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="cc970-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cc970-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="cc970-115">-Name</span></span>
<span data-ttu-id="cc970-116">Указывает имя частной зоны DNS, которую нужно создать.</span><span class="sxs-lookup"><span data-stu-id="cc970-116">Specifies the name of the private DNS zone to create.</span></span>

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

### <span data-ttu-id="cc970-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc970-117">-ResourceGroupName</span></span>
<span data-ttu-id="cc970-118">Указывает группу ресурсов, в которой нужно создать зону.</span><span class="sxs-lookup"><span data-stu-id="cc970-118">Specifies the resource group in which to create the zone.</span></span>

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

### <span data-ttu-id="cc970-119">-Тег</span><span class="sxs-lookup"><span data-stu-id="cc970-119">-Tag</span></span>
<span data-ttu-id="cc970-120">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cc970-120">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="cc970-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cc970-121">-Confirm</span></span>
<span data-ttu-id="cc970-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="cc970-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc970-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc970-123">-WhatIf</span></span>
<span data-ttu-id="cc970-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="cc970-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cc970-125">Командлет не выполняется. Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="cc970-125">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cc970-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="cc970-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc970-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc970-127">CommonParameters</span></span>
<span data-ttu-id="cc970-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cc970-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc970-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc970-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc970-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cc970-130">INPUTS</span></span>

### <span data-ttu-id="cc970-131">Ничего</span><span class="sxs-lookup"><span data-stu-id="cc970-131">None</span></span>

## <span data-ttu-id="cc970-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cc970-132">OUTPUTS</span></span>

### <span data-ttu-id="cc970-133">Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="cc970-133">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

## <span data-ttu-id="cc970-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="cc970-134">NOTES</span></span>

## <span data-ttu-id="cc970-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cc970-135">RELATED LINKS</span></span>

[<span data-ttu-id="cc970-136">Get-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="cc970-136">Get-AzPrivateDnsZone</span></span>](./Get-AzPrivateDnsZone.md)

[<span data-ttu-id="cc970-137">New-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="cc970-137">New-AzPrivateDnsRecordSet</span></span>](./New-AzPrivateDnsRecordSet.md)

[<span data-ttu-id="cc970-138">Remove-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="cc970-138">Remove-AzPrivateDnsZone</span></span>](./Remove-AzPrivateDnsZone.md)
