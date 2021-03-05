---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Set-AzSqlInformationProtectionPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSqlInformationProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSqlInformationProtectionPolicy.md
ms.openlocfilehash: 72ad39ef5b63482b10623c1945c0fb5280e07603
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986488"
---
# <span data-ttu-id="36f76-101">Set-AzSqlInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="36f76-101">Set-AzSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="36f76-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36f76-102">SYNOPSIS</span></span>
<span data-ttu-id="36f76-103">Задает эффективную политику SQL защиты информации.</span><span class="sxs-lookup"><span data-stu-id="36f76-103">Sets the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="36f76-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="36f76-104">SYNTAX</span></span>

### <span data-ttu-id="36f76-105">SQL политики защиты информации (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="36f76-105">SQL Information Protection Policy (Default)</span></span>
```
Set-AzSqlInformationProtectionPolicy -Policy <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36f76-106">SQL пути к файлу политики защиты информации</span><span class="sxs-lookup"><span data-stu-id="36f76-106">SQL Information Protection Policy File Path</span></span>
```
Set-AzSqlInformationProtectionPolicy -FilePath <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36f76-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="36f76-107">DESCRIPTION</span></span>
<span data-ttu-id="36f76-108">Задает эффективную политику SQL защиты информации.</span><span class="sxs-lookup"><span data-stu-id="36f76-108">Sets the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="36f76-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="36f76-109">EXAMPLES</span></span>

### <span data-ttu-id="36f76-110">Пример</span><span class="sxs-lookup"><span data-stu-id="36f76-110">Example</span></span>
```powershell
PS C:\> Set-AzSqlInformationProtectionPolicy -FilePath "C:\Users\myUser\Desktop\policy.json"
```

## <span data-ttu-id="36f76-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="36f76-111">PARAMETERS</span></span>

### <span data-ttu-id="36f76-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="36f76-112">-AsJob</span></span>
<span data-ttu-id="36f76-113">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="36f76-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="36f76-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36f76-114">-DefaultProfile</span></span>
<span data-ttu-id="36f76-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="36f76-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36f76-116">-FilePath</span><span class="sxs-lookup"><span data-stu-id="36f76-116">-FilePath</span></span>
<span data-ttu-id="36f76-117">Путь к JSON-файлу, содержащего SQL определения политики защиты информации.</span><span class="sxs-lookup"><span data-stu-id="36f76-117">Specifies a path of a .json file containing SQL Information Protection Policy definition.</span></span>

```yaml
Type: System.String
Parameter Sets: SQL Information Protection Policy File Path
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36f76-118">-Политика</span><span class="sxs-lookup"><span data-stu-id="36f76-118">-Policy</span></span>
<span data-ttu-id="36f76-119">Определяет определение политики SQL защиты информации.</span><span class="sxs-lookup"><span data-stu-id="36f76-119">Specifies a SQL information protection policy definition.</span></span> <span data-ttu-id="36f76-120">Вы можете указать путь к JSON-файлу или строке, определяемой политикой в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="36f76-120">You can specify a path of a .json file or a JSON format string that defines the policy.</span></span>

```yaml
Type: System.String
Parameter Sets: SQL Information Protection Policy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36f76-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="36f76-121">-Confirm</span></span>
<span data-ttu-id="36f76-122">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36f76-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36f76-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36f76-123">-WhatIf</span></span>
<span data-ttu-id="36f76-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36f76-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="36f76-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="36f76-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36f76-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36f76-126">CommonParameters</span></span>
<span data-ttu-id="36f76-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36f76-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36f76-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="36f76-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36f76-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="36f76-129">INPUTS</span></span>

### <span data-ttu-id="36f76-130">System.String</span><span class="sxs-lookup"><span data-stu-id="36f76-130">System.String</span></span>

## <span data-ttu-id="36f76-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="36f76-131">OUTPUTS</span></span>

### <span data-ttu-id="36f76-132">Microsoft.Azure.Commands.SecurityCenter.Models.SqlInformationProtectionPolicy.PSSqlInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="36f76-132">Microsoft.Azure.Commands.SecurityCenter.Models.SqlInformationProtectionPolicy.PSSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="36f76-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="36f76-133">NOTES</span></span>

## <span data-ttu-id="36f76-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="36f76-134">RELATED LINKS</span></span>
