---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeUser.md
ms.openlocfilehash: a53f67c12a5c8d125319fc19f69db3ea9a57c5e1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242853"
---
# <span data-ttu-id="16897-101">New-AzDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="16897-101">New-AzDataBoxEdgeUser</span></span>

## <span data-ttu-id="16897-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16897-102">SYNOPSIS</span></span>
<span data-ttu-id="16897-103">Создает нового пользователя для устройства.</span><span class="sxs-lookup"><span data-stu-id="16897-103">Creates a new user for the device.</span></span>

## <span data-ttu-id="16897-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="16897-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -Password <SecureString> -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [[-Type] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16897-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="16897-105">DESCRIPTION</span></span>
<span data-ttu-id="16897-106">С **новыми данными AzDataBoxEdgeUser** создается новый пользователь для устройства Edge Box Data Box.</span><span class="sxs-lookup"><span data-stu-id="16897-106">The **New-AzDataBoxEdgeUser** cmdlet creates a new user for the Data Box Edge device.</span></span> <span data-ttu-id="16897-107">Поддерживается создание только пользователей `Share` разных типов.</span><span class="sxs-lookup"><span data-stu-id="16897-107">Creation of only users of type `Share` is supported.</span></span>

## <span data-ttu-id="16897-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="16897-108">EXAMPLES</span></span>

### <span data-ttu-id="16897-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="16897-109">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
 -Password password-secured-string -EncryptionKey encryption-key
User name   Type  ResourceGroupName DeviceName
---------   ----  ----------------- ----------
username    Share resourceGroupName deviceName
```

```powershell
PS C:\> New-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
 -Password password-secured-string -EncryptionKey encryption-key -Type Share
User name   Type  ResourceGroupName DeviceName
---------   ----  ----------------- ----------
username    Share resourceGroupName deviceName
```

## <span data-ttu-id="16897-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="16897-110">PARAMETERS</span></span>

### <span data-ttu-id="16897-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="16897-111">-AsJob</span></span>
<span data-ttu-id="16897-112">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="16897-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="16897-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16897-113">-DefaultProfile</span></span>
<span data-ttu-id="16897-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="16897-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16897-115">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="16897-115">-DeviceName</span></span>
<span data-ttu-id="16897-116">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="16897-116">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16897-117">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="16897-117">-EncryptionKey</span></span>
<span data-ttu-id="16897-118">Ключ шифрования устройства Edge</span><span class="sxs-lookup"><span data-stu-id="16897-118">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="16897-119">-Name</span><span class="sxs-lookup"><span data-stu-id="16897-119">-Name</span></span>
<span data-ttu-id="16897-120">Имя пользователя</span><span class="sxs-lookup"><span data-stu-id="16897-120">Username</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16897-121">-Password</span><span class="sxs-lookup"><span data-stu-id="16897-121">-Password</span></span>
<span data-ttu-id="16897-122">Пароль в качестве защищенной строки</span><span class="sxs-lookup"><span data-stu-id="16897-122">Password, provide as a secure string</span></span>

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

### <span data-ttu-id="16897-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16897-123">-ResourceGroupName</span></span>
<span data-ttu-id="16897-124">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="16897-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16897-125">-Type</span><span class="sxs-lookup"><span data-stu-id="16897-125">-Type</span></span>
<span data-ttu-id="16897-126">Select UserType</span><span class="sxs-lookup"><span data-stu-id="16897-126">Select UserType</span></span>

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

### <span data-ttu-id="16897-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="16897-127">-Confirm</span></span>
<span data-ttu-id="16897-128">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="16897-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16897-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16897-129">-WhatIf</span></span>
<span data-ttu-id="16897-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="16897-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="16897-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="16897-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16897-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16897-132">CommonParameters</span></span>
<span data-ttu-id="16897-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16897-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16897-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="16897-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16897-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="16897-135">INPUTS</span></span>

### <span data-ttu-id="16897-136">Нет</span><span class="sxs-lookup"><span data-stu-id="16897-136">None</span></span>

## <span data-ttu-id="16897-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="16897-137">OUTPUTS</span></span>

### <span data-ttu-id="16897-138">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="16897-138">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="16897-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="16897-139">NOTES</span></span>

## <span data-ttu-id="16897-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="16897-140">RELATED LINKS</span></span>
