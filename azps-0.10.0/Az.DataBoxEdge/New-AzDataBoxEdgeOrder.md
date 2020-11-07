---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeOrder.md
ms.openlocfilehash: 6e9aa41b30b9a2012e4208971ceddff8f08e980a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911270"
---
# <span data-ttu-id="aa97a-101">New-AzDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="aa97a-101">New-AzDataBoxEdgeOrder</span></span>

## <span data-ttu-id="aa97a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="aa97a-102">SYNOPSIS</span></span>
<span data-ttu-id="aa97a-103">Создание нового заказа для устройства.</span><span class="sxs-lookup"><span data-stu-id="aa97a-103">Creates a new order for a device.</span></span>

## <span data-ttu-id="aa97a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="aa97a-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String> -ContactPerson <String>
 -CompanyName <String> -Phone <String> -Email <String[]> -AddressLine1 <String> -PostalCode <String>
 -City <String> -State <String> -Country <String> [-AddressLine2 <String>] [-AddressLine3 <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa97a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="aa97a-105">DESCRIPTION</span></span>
<span data-ttu-id="aa97a-106">Командлет **New-AzDataBoxEdgeOrder** создает новый заказ на пограничном устройстве для поля данных.</span><span class="sxs-lookup"><span data-stu-id="aa97a-106">The **New-AzDataBoxEdgeOrder** cmdlet creates a new order for a Data Box Edge device.</span></span> <span data-ttu-id="aa97a-107">Прежде чем создавать заказ, необходимо сначала создать ресурс устройства "поле данных".</span><span class="sxs-lookup"><span data-stu-id="aa97a-107">A Data Box Edge device resource needs to be created first before creating an order.</span></span> <span data-ttu-id="aa97a-108">Вы можете указать такие сведения, как Контактное лицо, название компании, адрес электронной почты и т. д. в качестве параметров создания заказа.</span><span class="sxs-lookup"><span data-stu-id="aa97a-108">You can specify details like contact person, company name, email, address etc. as parameters for creating the order.�</span></span>

## <span data-ttu-id="aa97a-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="aa97a-109">EXAMPLES</span></span>

### <span data-ttu-id="aa97a-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="aa97a-110">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeOrder -ResourceGroupName rg-name -DeviceName device-name -ContactPerson "John Mcclane" -CompanyName Microsoft -Phone 8004269400 -Email john@microsoft.com -AddressLine1  "Microsoft Corporation" -PostalCode 98052 -City Redmond -State WA -Country USA
DeviceName  ResourceGroupName Status    UpdatedDatetime
----------  ----------------- ------    ---------------
deviceName  resourceGroupName Untracked 01-Jan-01 12:00:00 AM
```

## <span data-ttu-id="aa97a-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="aa97a-111">PARAMETERS</span></span>

### <span data-ttu-id="aa97a-112">-AddressLine1</span><span class="sxs-lookup"><span data-stu-id="aa97a-112">-AddressLine1</span></span>
<span data-ttu-id="aa97a-113">Адрес первой строки</span><span class="sxs-lookup"><span data-stu-id="aa97a-113">Address first line</span></span>

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

### <span data-ttu-id="aa97a-114">-AddressLine2</span><span class="sxs-lookup"><span data-stu-id="aa97a-114">-AddressLine2</span></span>
<span data-ttu-id="aa97a-115">Адресная вторая строка</span><span class="sxs-lookup"><span data-stu-id="aa97a-115">Address second line</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa97a-116">-AddressLine3</span><span class="sxs-lookup"><span data-stu-id="aa97a-116">-AddressLine3</span></span>
<span data-ttu-id="aa97a-117">Адрес третьей строки</span><span class="sxs-lookup"><span data-stu-id="aa97a-117">Address third line</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa97a-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aa97a-118">-AsJob</span></span>
<span data-ttu-id="aa97a-119">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="aa97a-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="aa97a-120">-Город</span><span class="sxs-lookup"><span data-stu-id="aa97a-120">-City</span></span>
<span data-ttu-id="aa97a-121">Название города</span><span class="sxs-lookup"><span data-stu-id="aa97a-121">Name of the City</span></span>

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

### <span data-ttu-id="aa97a-122">-CompanyName</span><span class="sxs-lookup"><span data-stu-id="aa97a-122">-CompanyName</span></span>
<span data-ttu-id="aa97a-123">Название компании</span><span class="sxs-lookup"><span data-stu-id="aa97a-123">Name of the company</span></span>

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

### <span data-ttu-id="aa97a-124">-ContactPerson</span><span class="sxs-lookup"><span data-stu-id="aa97a-124">-ContactPerson</span></span>
<span data-ttu-id="aa97a-125">Имя контактного лица</span><span class="sxs-lookup"><span data-stu-id="aa97a-125">Name of the contact person</span></span>

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

### <span data-ttu-id="aa97a-126">-Country</span><span class="sxs-lookup"><span data-stu-id="aa97a-126">-Country</span></span>
<span data-ttu-id="aa97a-127">Название страны</span><span class="sxs-lookup"><span data-stu-id="aa97a-127">Name of the Country</span></span>

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

### <span data-ttu-id="aa97a-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa97a-128">-DefaultProfile</span></span>
<span data-ttu-id="aa97a-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="aa97a-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa97a-130">-Имя_устройства</span><span class="sxs-lookup"><span data-stu-id="aa97a-130">-DeviceName</span></span>
<span data-ttu-id="aa97a-131">Название ресурса</span><span class="sxs-lookup"><span data-stu-id="aa97a-131">Resource Name</span></span>

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

### <span data-ttu-id="aa97a-132">-Электронная почта</span><span class="sxs-lookup"><span data-stu-id="aa97a-132">-Email</span></span>
<span data-ttu-id="aa97a-133">Список сообщений электронной почты, чтобы получать обновления, может содержать не более 10 сообщений электронной почты</span><span class="sxs-lookup"><span data-stu-id="aa97a-133">List of Emails to receive updates, Accepts max of 10 emails</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa97a-134">-Phone</span><span class="sxs-lookup"><span data-stu-id="aa97a-134">-Phone</span></span>
<span data-ttu-id="aa97a-135">Номер телефона контактного лица</span><span class="sxs-lookup"><span data-stu-id="aa97a-135">Phone number of the contact person</span></span>

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

### <span data-ttu-id="aa97a-136">-PostalCode</span><span class="sxs-lookup"><span data-stu-id="aa97a-136">-PostalCode</span></span>
<span data-ttu-id="aa97a-137">Почтовый индекс адреса</span><span class="sxs-lookup"><span data-stu-id="aa97a-137">Postal Code of the Address</span></span>

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

### <span data-ttu-id="aa97a-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa97a-138">-ResourceGroupName</span></span>
<span data-ttu-id="aa97a-139">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="aa97a-139">Resource Group Name</span></span>

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

### <span data-ttu-id="aa97a-140">-State</span><span class="sxs-lookup"><span data-stu-id="aa97a-140">-State</span></span>
<span data-ttu-id="aa97a-141">Название состояния</span><span class="sxs-lookup"><span data-stu-id="aa97a-141">Name of the State</span></span>

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

### <span data-ttu-id="aa97a-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aa97a-142">-Confirm</span></span>
<span data-ttu-id="aa97a-143">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="aa97a-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa97a-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa97a-144">-WhatIf</span></span>
<span data-ttu-id="aa97a-145">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="aa97a-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aa97a-146">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="aa97a-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa97a-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa97a-147">CommonParameters</span></span>
<span data-ttu-id="aa97a-148">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="aa97a-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa97a-149">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aa97a-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa97a-150">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="aa97a-150">INPUTS</span></span>

### <span data-ttu-id="aa97a-151">System. String</span><span class="sxs-lookup"><span data-stu-id="aa97a-151">System.String</span></span>

## <span data-ttu-id="aa97a-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="aa97a-152">OUTPUTS</span></span>

### <span data-ttu-id="aa97a-153">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="aa97a-153">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span></span>

## <span data-ttu-id="aa97a-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="aa97a-154">NOTES</span></span>

## <span data-ttu-id="aa97a-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="aa97a-155">RELATED LINKS</span></span>
