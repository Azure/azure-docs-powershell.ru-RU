---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeUser.md
ms.openlocfilehash: 244adfb2707d47cef56390ce0d707b9f51fe229b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504960"
---
# <span data-ttu-id="463aa-101">New-AzStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="463aa-101">New-AzStackEdgeUser</span></span>

## <span data-ttu-id="463aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="463aa-102">SYNOPSIS</span></span>
<span data-ttu-id="463aa-103">Создает нового пользователя для устройства.</span><span class="sxs-lookup"><span data-stu-id="463aa-103">Creates a new user for the device.</span></span>

## <span data-ttu-id="463aa-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="463aa-104">SYNTAX</span></span>

```
New-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -Password <SecureString> -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [[-Type] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="463aa-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="463aa-105">DESCRIPTION</span></span>
<span data-ttu-id="463aa-106">Для устройства Stack Edge создается новый пользователь — **New-AzStackEdgeUser.**</span><span class="sxs-lookup"><span data-stu-id="463aa-106">The **New-AzStackEdgeUser** cmdlet creates a new user for the Stack Edge device.</span></span> <span data-ttu-id="463aa-107">Поддерживается создание только пользователей `Share` разных типов.</span><span class="sxs-lookup"><span data-stu-id="463aa-107">Creation of only users of type `Share` is supported.</span></span>

## <span data-ttu-id="463aa-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="463aa-108">EXAMPLES</span></span>

### <span data-ttu-id="463aa-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="463aa-109">Example 1</span></span>
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

## <span data-ttu-id="463aa-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="463aa-110">PARAMETERS</span></span>

### <span data-ttu-id="463aa-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="463aa-111">-AsJob</span></span>
<span data-ttu-id="463aa-112">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="463aa-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="463aa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="463aa-113">-DefaultProfile</span></span>
<span data-ttu-id="463aa-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="463aa-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="463aa-115">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="463aa-115">-DeviceName</span></span>
<span data-ttu-id="463aa-116">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="463aa-116">Device Name</span></span>

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

### <span data-ttu-id="463aa-117">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="463aa-117">-EncryptionKey</span></span>
<span data-ttu-id="463aa-118">Ключ шифрования устройства Edge</span><span class="sxs-lookup"><span data-stu-id="463aa-118">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="463aa-119">-Name</span><span class="sxs-lookup"><span data-stu-id="463aa-119">-Name</span></span>
<span data-ttu-id="463aa-120">Имя пользователя</span><span class="sxs-lookup"><span data-stu-id="463aa-120">Username</span></span>

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

### <span data-ttu-id="463aa-121">-Password</span><span class="sxs-lookup"><span data-stu-id="463aa-121">-Password</span></span>
<span data-ttu-id="463aa-122">Пароль в качестве защищенной строки</span><span class="sxs-lookup"><span data-stu-id="463aa-122">Password, provide as a secure string</span></span>

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

### <span data-ttu-id="463aa-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="463aa-123">-ResourceGroupName</span></span>
<span data-ttu-id="463aa-124">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="463aa-124">Resource Group Name</span></span>

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

### <span data-ttu-id="463aa-125">-Type</span><span class="sxs-lookup"><span data-stu-id="463aa-125">-Type</span></span>
<span data-ttu-id="463aa-126">Select UserType</span><span class="sxs-lookup"><span data-stu-id="463aa-126">Select UserType</span></span>

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

### <span data-ttu-id="463aa-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="463aa-127">-Confirm</span></span>
<span data-ttu-id="463aa-128">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="463aa-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="463aa-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="463aa-129">-WhatIf</span></span>
<span data-ttu-id="463aa-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="463aa-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="463aa-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="463aa-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="463aa-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="463aa-132">CommonParameters</span></span>
<span data-ttu-id="463aa-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="463aa-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="463aa-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="463aa-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="463aa-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="463aa-135">INPUTS</span></span>

### <span data-ttu-id="463aa-136">Нет</span><span class="sxs-lookup"><span data-stu-id="463aa-136">None</span></span>

## <span data-ttu-id="463aa-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="463aa-137">OUTPUTS</span></span>

### <span data-ttu-id="463aa-138">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="463aa-138">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="463aa-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="463aa-139">NOTES</span></span>

## <span data-ttu-id="463aa-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="463aa-140">RELATED LINKS</span></span>
