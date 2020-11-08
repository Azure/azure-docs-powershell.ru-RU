---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeUser.md
ms.openlocfilehash: 244adfb2707d47cef56390ce0d707b9f51fe229b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243824"
---
# <span data-ttu-id="a95cd-101">New-AzStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="a95cd-101">New-AzStackEdgeUser</span></span>

## <span data-ttu-id="a95cd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a95cd-102">SYNOPSIS</span></span>
<span data-ttu-id="a95cd-103">Создание нового пользователя для устройства.</span><span class="sxs-lookup"><span data-stu-id="a95cd-103">Creates a new user for the device.</span></span>

## <span data-ttu-id="a95cd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a95cd-104">SYNTAX</span></span>

```
New-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -Password <SecureString> -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [[-Type] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a95cd-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a95cd-105">DESCRIPTION</span></span>
<span data-ttu-id="a95cd-106">Командлет **New-AzStackEdgeUser** создает нового пользователя для краевого устройства стека.</span><span class="sxs-lookup"><span data-stu-id="a95cd-106">The **New-AzStackEdgeUser** cmdlet creates a new user for the Stack Edge device.</span></span> <span data-ttu-id="a95cd-107">Поддерживается создание только пользователей типа `Share` .</span><span class="sxs-lookup"><span data-stu-id="a95cd-107">Creation of only users of type `Share` is supported.</span></span>

## <span data-ttu-id="a95cd-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a95cd-108">EXAMPLES</span></span>

### <span data-ttu-id="a95cd-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a95cd-109">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
 -Password password-secured-string -EncryptionKey encryption-key
User name   Type  ResourceGroupName DeviceName
---------   ----  ----------------- ----------
username    Share resourceGroupName deviceName
```

```powershell
PS C:\> New-AzStackEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
 -Password password-secured-string -EncryptionKey encryption-key -Type Share
User name   Type  ResourceGroupName DeviceName
---------   ----  ----------------- ----------
username    Share resourceGroupName deviceName
```

## <span data-ttu-id="a95cd-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a95cd-110">PARAMETERS</span></span>

### <span data-ttu-id="a95cd-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a95cd-111">-AsJob</span></span>
<span data-ttu-id="a95cd-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="a95cd-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a95cd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a95cd-113">-DefaultProfile</span></span>
<span data-ttu-id="a95cd-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a95cd-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a95cd-115">-Имя_устройства</span><span class="sxs-lookup"><span data-stu-id="a95cd-115">-DeviceName</span></span>
<span data-ttu-id="a95cd-116">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="a95cd-116">Device Name</span></span>

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

### <span data-ttu-id="a95cd-117">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="a95cd-117">-EncryptionKey</span></span>
<span data-ttu-id="a95cd-118">Ключ шифрования на пограничном устройстве</span><span class="sxs-lookup"><span data-stu-id="a95cd-118">Encryption key of the Edge device</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a95cd-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a95cd-119">-Name</span></span>
<span data-ttu-id="a95cd-120">Действительно</span><span class="sxs-lookup"><span data-stu-id="a95cd-120">Username</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Username

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a95cd-121">-Password (пароль)</span><span class="sxs-lookup"><span data-stu-id="a95cd-121">-Password</span></span>
<span data-ttu-id="a95cd-122">Пароль, предоставление в качестве безопасной строки</span><span class="sxs-lookup"><span data-stu-id="a95cd-122">Password, provide as a secure string</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a95cd-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a95cd-123">-ResourceGroupName</span></span>
<span data-ttu-id="a95cd-124">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="a95cd-124">Resource Group Name</span></span>

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

### <span data-ttu-id="a95cd-125">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="a95cd-125">-Type</span></span>
<span data-ttu-id="a95cd-126">Выбор UserType</span><span class="sxs-lookup"><span data-stu-id="a95cd-126">Select UserType</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a95cd-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a95cd-127">-Confirm</span></span>
<span data-ttu-id="a95cd-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a95cd-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a95cd-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a95cd-129">-WhatIf</span></span>
<span data-ttu-id="a95cd-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a95cd-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a95cd-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a95cd-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a95cd-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a95cd-132">CommonParameters</span></span>
<span data-ttu-id="a95cd-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a95cd-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a95cd-134">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a95cd-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a95cd-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a95cd-135">INPUTS</span></span>

### <span data-ttu-id="a95cd-136">Ничего</span><span class="sxs-lookup"><span data-stu-id="a95cd-136">None</span></span>

## <span data-ttu-id="a95cd-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a95cd-137">OUTPUTS</span></span>

### <span data-ttu-id="a95cd-138">Microsoft. Azure. PowerShell. командлеты. StackEdge. Models. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="a95cd-138">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="a95cd-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="a95cd-139">NOTES</span></span>

## <span data-ttu-id="a95cd-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a95cd-140">RELATED LINKS</span></span>
