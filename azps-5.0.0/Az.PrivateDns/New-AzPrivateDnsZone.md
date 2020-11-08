---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/new-azprivatednszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsZone.md
ms.openlocfilehash: 98830e2dbcfc115cd026c33782030bc40fa6763f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248492"
---
# <span data-ttu-id="5e14b-101">New-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="5e14b-101">New-AzPrivateDnsZone</span></span>

## <span data-ttu-id="5e14b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5e14b-102">SYNOPSIS</span></span>
<span data-ttu-id="5e14b-103">Создание частной зоны DNS.</span><span class="sxs-lookup"><span data-stu-id="5e14b-103">Creates a new private DNS zone.</span></span>

## <span data-ttu-id="5e14b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5e14b-104">SYNTAX</span></span>

```
New-AzPrivateDnsZone -ResourceGroupName <String> -Name <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e14b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5e14b-105">DESCRIPTION</span></span>
<span data-ttu-id="5e14b-106">Командлет **New-AzPrivateDnsZone** создает новую зону DNS (Private Domain Name System) в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5e14b-106">The **New-AzPrivateDnsZone** cmdlet creates a new private Domain Name System (DNS) zone in the specified resource group.</span></span> <span data-ttu-id="5e14b-107">Для параметра *Name* необходимо указать уникальное имя частной зоны DNS или командлет будет возвращать ошибку.</span><span class="sxs-lookup"><span data-stu-id="5e14b-107">You must specify a unique private DNS zone name for the *Name* parameter or the cmdlet will return an error.</span></span> <span data-ttu-id="5e14b-108">После создания зоны используйте командлет New-AzPrivateDnsRecordSet для создания наборов записей в зоне.</span><span class="sxs-lookup"><span data-stu-id="5e14b-108">After the zone is created, use the New-AzPrivateDnsRecordSet cmdlet to create record sets in the zone.</span></span>
<span data-ttu-id="5e14b-109">Вы можете использовать параметр *Confirm* и $ConfirmPreference переменной Windows PowerShell, чтобы указать, нужно ли командлету запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="5e14b-109">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="5e14b-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5e14b-110">EXAMPLES</span></span>

### <span data-ttu-id="5e14b-111">Пример 1: создание частной зоны DNS</span><span class="sxs-lookup"><span data-stu-id="5e14b-111">Example 1: Create a Private DNS zone</span></span>
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

## <span data-ttu-id="5e14b-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5e14b-112">PARAMETERS</span></span>

### <span data-ttu-id="5e14b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e14b-113">-DefaultProfile</span></span>
<span data-ttu-id="5e14b-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="5e14b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5e14b-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5e14b-115">-Name</span></span>
<span data-ttu-id="5e14b-116">Указывает имя частной зоны DNS, которую нужно создать.</span><span class="sxs-lookup"><span data-stu-id="5e14b-116">Specifies the name of the private DNS zone to create.</span></span>

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

### <span data-ttu-id="5e14b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e14b-117">-ResourceGroupName</span></span>
<span data-ttu-id="5e14b-118">Указывает группу ресурсов, в которой нужно создать зону.</span><span class="sxs-lookup"><span data-stu-id="5e14b-118">Specifies the resource group in which to create the zone.</span></span>

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

### <span data-ttu-id="5e14b-119">-Тег</span><span class="sxs-lookup"><span data-stu-id="5e14b-119">-Tag</span></span>
<span data-ttu-id="5e14b-120">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5e14b-120">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="5e14b-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5e14b-121">-Confirm</span></span>
<span data-ttu-id="5e14b-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5e14b-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e14b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e14b-123">-WhatIf</span></span>
<span data-ttu-id="5e14b-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5e14b-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5e14b-125">Командлет не выполняется. Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5e14b-125">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5e14b-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5e14b-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e14b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e14b-127">CommonParameters</span></span>
<span data-ttu-id="5e14b-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5e14b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e14b-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e14b-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e14b-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5e14b-130">INPUTS</span></span>

### <span data-ttu-id="5e14b-131">Ничего</span><span class="sxs-lookup"><span data-stu-id="5e14b-131">None</span></span>

## <span data-ttu-id="5e14b-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5e14b-132">OUTPUTS</span></span>

### <span data-ttu-id="5e14b-133">Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="5e14b-133">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

## <span data-ttu-id="5e14b-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="5e14b-134">NOTES</span></span>

## <span data-ttu-id="5e14b-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5e14b-135">RELATED LINKS</span></span>

[<span data-ttu-id="5e14b-136">Get-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="5e14b-136">Get-AzPrivateDnsZone</span></span>](./Get-AzPrivateDnsZone.md)

[<span data-ttu-id="5e14b-137">New-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="5e14b-137">New-AzPrivateDnsRecordSet</span></span>](./New-AzPrivateDnsRecordSet.md)

[<span data-ttu-id="5e14b-138">Remove-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="5e14b-138">Remove-AzPrivateDnsZone</span></span>](./Remove-AzPrivateDnsZone.md)
