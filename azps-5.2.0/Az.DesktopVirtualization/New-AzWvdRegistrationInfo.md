---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdRegistrationInfo.md
ms.openlocfilehash: 2268135ebd1e1c504aae7462730d104e842f288f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98392863"
---
# <span data-ttu-id="39a86-101">New-AzWvdRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="39a86-101">New-AzWvdRegistrationInfo</span></span>

## <span data-ttu-id="39a86-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39a86-102">SYNOPSIS</span></span>
<span data-ttu-id="39a86-103">Создайте сведения о регистрации виртуальных рабочих стола Windows.</span><span class="sxs-lookup"><span data-stu-id="39a86-103">Create Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="39a86-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="39a86-104">SYNTAX</span></span>

```
New-AzWvdRegistrationInfo -ExpirationTime <String> -HostPoolName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="39a86-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="39a86-105">DESCRIPTION</span></span>
<span data-ttu-id="39a86-106">Создайте сведения о регистрации виртуальных рабочих стола Windows.</span><span class="sxs-lookup"><span data-stu-id="39a86-106">Create Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="39a86-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="39a86-107">EXAMPLES</span></span>

### <span data-ttu-id="39a86-108">Пример 1. Создание маркера регистрации виртуального рабочего стола Windows</span><span class="sxs-lookup"><span data-stu-id="39a86-108">Example 1: Create a Windows Virtual Desktop Registration Token</span></span>
```powershell
PS C:\> New-AzWvdRegistrationInfo -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -ExpirationTime $((get-date).ToUniversalTime().AddDays(1).ToString('yyyy-MM-ddTHH:mm:ss.fffffffZ'))

ExpirationTime       RegistrationTokenOperation Token
--------------       -------------------------- -----
4/1/2020 10:19:33 PM Update                       eyJhbGciOiJSUzI1NiIsImtpZCI6IkMyRjU1RUYxNzg0MEFCNzkzMDk2RUYzRjdEMkNBRDk0NThGNDhEOTQiLCJ0eXAiOiJKV1QifQ.eyJSZWdpc3RyYXRpb25JZCI6IjU5NGJjZWUwLTk5MjQtNDg3ZC1iOW...
```

<span data-ttu-id="39a86-109">Эта команда создает маркер регистрации виртуального рабочего стола Windows в пуле хостов.</span><span class="sxs-lookup"><span data-stu-id="39a86-109">This command creates a Windows Virtual Desktop Registration Token in a Host Pool.</span></span>

## <span data-ttu-id="39a86-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="39a86-110">PARAMETERS</span></span>

### <span data-ttu-id="39a86-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39a86-111">-DefaultProfile</span></span>
<span data-ttu-id="39a86-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="39a86-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39a86-113">-ExpirationTime</span><span class="sxs-lookup"><span data-stu-id="39a86-113">-ExpirationTime</span></span>
<span data-ttu-id="39a86-114">Срок действия</span><span class="sxs-lookup"><span data-stu-id="39a86-114">Expiration Time</span></span>

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

### <span data-ttu-id="39a86-115">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="39a86-115">-HostPoolName</span></span>
<span data-ttu-id="39a86-116">Host Pool Name</span><span class="sxs-lookup"><span data-stu-id="39a86-116">Host Pool Name</span></span>

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

### <span data-ttu-id="39a86-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39a86-117">-ResourceGroupName</span></span>
<span data-ttu-id="39a86-118">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="39a86-118">Resource Group Name</span></span>

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

### <span data-ttu-id="39a86-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="39a86-119">-SubscriptionId</span></span>
<span data-ttu-id="39a86-120">ИД подписки</span><span class="sxs-lookup"><span data-stu-id="39a86-120">Subscription Id</span></span>

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

### <span data-ttu-id="39a86-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="39a86-121">-Confirm</span></span>
<span data-ttu-id="39a86-122">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39a86-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39a86-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39a86-123">-WhatIf</span></span>
<span data-ttu-id="39a86-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39a86-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39a86-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="39a86-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39a86-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39a86-126">CommonParameters</span></span>
<span data-ttu-id="39a86-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39a86-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39a86-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="39a86-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39a86-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="39a86-129">INPUTS</span></span>

## <span data-ttu-id="39a86-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="39a86-130">OUTPUTS</span></span>

### <span data-ttu-id="39a86-131">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="39a86-131">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IRegistrationInfo</span></span>

## <span data-ttu-id="39a86-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="39a86-132">NOTES</span></span>

<span data-ttu-id="39a86-133">ALIASES</span><span class="sxs-lookup"><span data-stu-id="39a86-133">ALIASES</span></span>

## <span data-ttu-id="39a86-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="39a86-134">RELATED LINKS</span></span>

