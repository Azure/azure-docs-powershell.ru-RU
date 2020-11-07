---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeUser.md
ms.openlocfilehash: 480c0a8e932b672542595983f33fd19bab6fec3b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911257"
---
# <span data-ttu-id="c332f-101">New-AzDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="c332f-101">New-AzDataBoxEdgeUser</span></span>

## <span data-ttu-id="c332f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c332f-102">SYNOPSIS</span></span>
<span data-ttu-id="c332f-103">Создание нового пользователя для устройства.</span><span class="sxs-lookup"><span data-stu-id="c332f-103">Creates a new user for the device.</span></span>

## <span data-ttu-id="c332f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c332f-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -Password <SecureString> -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [[-Type] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c332f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c332f-105">DESCRIPTION</span></span>
<span data-ttu-id="c332f-106">Командлет **New-AzDataBoxEdgeUser** создает нового пользователя для устройства "поле данных".</span><span class="sxs-lookup"><span data-stu-id="c332f-106">The **New-AzDataBoxEdgeUser** cmdlet creates a new user for the Data Box Edge device.</span></span> <span data-ttu-id="c332f-107">Поддерживается создание только пользователей типа `Share` .</span><span class="sxs-lookup"><span data-stu-id="c332f-107">Creation of only users of type `Share` is supported.</span></span>

## <span data-ttu-id="c332f-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c332f-108">EXAMPLES</span></span>

### <span data-ttu-id="c332f-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c332f-109">Example 1</span></span>
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

## <span data-ttu-id="c332f-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c332f-110">PARAMETERS</span></span>

### <span data-ttu-id="c332f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c332f-111">-AsJob</span></span>
<span data-ttu-id="c332f-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="c332f-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c332f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c332f-113">-DefaultProfile</span></span>
<span data-ttu-id="c332f-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c332f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c332f-115">-Имя_устройства</span><span class="sxs-lookup"><span data-stu-id="c332f-115">-DeviceName</span></span>
<span data-ttu-id="c332f-116">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="c332f-116">Device Name</span></span>

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

### <span data-ttu-id="c332f-117">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="c332f-117">-EncryptionKey</span></span>
<span data-ttu-id="c332f-118">Ключ шифрования на пограничном устройстве</span><span class="sxs-lookup"><span data-stu-id="c332f-118">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="c332f-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c332f-119">-Name</span></span>
<span data-ttu-id="c332f-120">Действительно</span><span class="sxs-lookup"><span data-stu-id="c332f-120">Username</span></span>

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

### <span data-ttu-id="c332f-121">-Password (пароль)</span><span class="sxs-lookup"><span data-stu-id="c332f-121">-Password</span></span>
<span data-ttu-id="c332f-122">Пароль, предоставление в качестве безопасной строки</span><span class="sxs-lookup"><span data-stu-id="c332f-122">Password, provide as a secure string</span></span>

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

### <span data-ttu-id="c332f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c332f-123">-ResourceGroupName</span></span>
<span data-ttu-id="c332f-124">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="c332f-124">Resource Group Name</span></span>

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

### <span data-ttu-id="c332f-125">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="c332f-125">-Type</span></span>
<span data-ttu-id="c332f-126">Выбор UserType</span><span class="sxs-lookup"><span data-stu-id="c332f-126">Select UserType</span></span>

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

### <span data-ttu-id="c332f-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c332f-127">-Confirm</span></span>
<span data-ttu-id="c332f-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c332f-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c332f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c332f-129">-WhatIf</span></span>
<span data-ttu-id="c332f-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c332f-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c332f-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c332f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c332f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c332f-132">CommonParameters</span></span>
<span data-ttu-id="c332f-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c332f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c332f-134">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c332f-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c332f-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c332f-135">INPUTS</span></span>

### <span data-ttu-id="c332f-136">Ничего</span><span class="sxs-lookup"><span data-stu-id="c332f-136">None</span></span>

## <span data-ttu-id="c332f-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c332f-137">OUTPUTS</span></span>

### <span data-ttu-id="c332f-138">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="c332f-138">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="c332f-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="c332f-139">NOTES</span></span>

## <span data-ttu-id="c332f-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c332f-140">RELATED LINKS</span></span>
