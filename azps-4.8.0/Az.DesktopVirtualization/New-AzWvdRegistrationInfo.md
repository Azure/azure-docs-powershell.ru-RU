---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdRegistrationInfo.md
ms.openlocfilehash: 86ffd1038d834d20837b1f6a6087176e562c8844
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94245014"
---
# <span data-ttu-id="f0289-101">New-AzWvdRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="f0289-101">New-AzWvdRegistrationInfo</span></span>

## <span data-ttu-id="f0289-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f0289-102">SYNOPSIS</span></span>
<span data-ttu-id="f0289-103">Создание регистрационных данных виртуальных рабочих столов Windows.</span><span class="sxs-lookup"><span data-stu-id="f0289-103">Create Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="f0289-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f0289-104">SYNTAX</span></span>

```
New-AzWvdRegistrationInfo -ExpirationTime <String> -HostPoolName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f0289-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f0289-105">DESCRIPTION</span></span>
<span data-ttu-id="f0289-106">Создание регистрационных данных виртуальных рабочих столов Windows.</span><span class="sxs-lookup"><span data-stu-id="f0289-106">Create Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="f0289-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f0289-107">EXAMPLES</span></span>

### <span data-ttu-id="f0289-108">Пример 1: создание маркера регистрации виртуальных рабочих столов Windows</span><span class="sxs-lookup"><span data-stu-id="f0289-108">Example 1: Create a Windows Virtual Desktop Registration Token</span></span>
```powershell
PS C:\> New-AzWvdRegistrationInfo -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -ExpirationTime $((get-date).ToUniversalTime().AddDays(1).ToString('yyyy-MM-ddTHH:mm:ss.fffffffZ'))

ExpirationTime       RegistrationTokenOperation Token
--------------       -------------------------- -----
4/1/2020 10:19:33 PM Update                       eyJhbGciOiJSUzI1NiIsImtpZCI6IkMyRjU1RUYxNzg0MEFCNzkzMDk2RUYzRjdEMkNBRDk0NThGNDhEOTQiLCJ0eXAiOiJKV1QifQ.eyJSZWdpc3RyYXRpb25JZCI6IjU5NGJjZWUwLTk5MjQtNDg3ZC1iOW...
```

<span data-ttu-id="f0289-109">Эта команда создает маркер регистрации виртуальных рабочих столов для Windows в пуле узлов.</span><span class="sxs-lookup"><span data-stu-id="f0289-109">This command creates a Windows Virtual Desktop Registration Token in a Host Pool.</span></span>

## <span data-ttu-id="f0289-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f0289-110">PARAMETERS</span></span>

### <span data-ttu-id="f0289-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0289-111">-DefaultProfile</span></span>
<span data-ttu-id="f0289-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f0289-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0289-113">-ExpirationTime</span><span class="sxs-lookup"><span data-stu-id="f0289-113">-ExpirationTime</span></span>
<span data-ttu-id="f0289-114">Срок действия</span><span class="sxs-lookup"><span data-stu-id="f0289-114">Expiration Time</span></span>

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

### <span data-ttu-id="f0289-115">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="f0289-115">-HostPoolName</span></span>
<span data-ttu-id="f0289-116">Имя пула узлов</span><span class="sxs-lookup"><span data-stu-id="f0289-116">Host Pool Name</span></span>

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

### <span data-ttu-id="f0289-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0289-117">-ResourceGroupName</span></span>
<span data-ttu-id="f0289-118">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="f0289-118">Resource Group Name</span></span>

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

### <span data-ttu-id="f0289-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f0289-119">-SubscriptionId</span></span>
<span data-ttu-id="f0289-120">Идентификатор подписки</span><span class="sxs-lookup"><span data-stu-id="f0289-120">Subscription Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0289-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f0289-121">-Confirm</span></span>
<span data-ttu-id="f0289-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f0289-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0289-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0289-123">-WhatIf</span></span>
<span data-ttu-id="f0289-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f0289-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0289-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f0289-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0289-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0289-126">CommonParameters</span></span>
<span data-ttu-id="f0289-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f0289-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0289-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f0289-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0289-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f0289-129">INPUTS</span></span>

## <span data-ttu-id="f0289-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f0289-130">OUTPUTS</span></span>

### <span data-ttu-id="f0289-131">Microsoft. Azure. PowerShell. командлеты. DesktopVirtualization. Models. Api20191210Preview. IRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="f0289-131">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IRegistrationInfo</span></span>

## <span data-ttu-id="f0289-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="f0289-132">NOTES</span></span>

<span data-ttu-id="f0289-133">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="f0289-133">ALIASES</span></span>

## <span data-ttu-id="f0289-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f0289-134">RELATED LINKS</span></span>

