---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSqlInformationProtectionPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSqlInformationProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSqlInformationProtectionPolicy.md
ms.openlocfilehash: 3b433860cda56f827bb58bc135240da41b89ef93
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98394332"
---
# <span data-ttu-id="e4b0f-101">Set-AzSqlInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="e4b0f-101">Set-AzSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="e4b0f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4b0f-102">SYNOPSIS</span></span>
<span data-ttu-id="e4b0f-103">Задает эффективную политику SQL защиты информации.</span><span class="sxs-lookup"><span data-stu-id="e4b0f-103">Sets the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="e4b0f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e4b0f-104">SYNTAX</span></span>

### <span data-ttu-id="e4b0f-105">SQL политики защиты информации (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e4b0f-105">SQL Information Protection Policy (Default)</span></span>
```
Set-AzSqlInformationProtectionPolicy -Policy <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4b0f-106">SQL пути к файлу политики защиты информации</span><span class="sxs-lookup"><span data-stu-id="e4b0f-106">SQL Information Protection Policy File Path</span></span>
```
Set-AzSqlInformationProtectionPolicy -FilePath <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4b0f-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e4b0f-107">DESCRIPTION</span></span>
<span data-ttu-id="e4b0f-108">Задает эффективную политику SQL защиты информации.</span><span class="sxs-lookup"><span data-stu-id="e4b0f-108">Sets the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="e4b0f-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e4b0f-109">EXAMPLES</span></span>

### <span data-ttu-id="e4b0f-110">Пример</span><span class="sxs-lookup"><span data-stu-id="e4b0f-110">Example</span></span>
```powershell
PS C:\> Set-AzSqlInformationProtectionPolicy -FilePath "C:\Users\myUser\Desktop\policy.json"
```

## <span data-ttu-id="e4b0f-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e4b0f-111">PARAMETERS</span></span>

### <span data-ttu-id="e4b0f-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e4b0f-112">-AsJob</span></span>
<span data-ttu-id="e4b0f-113">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="e4b0f-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e4b0f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4b0f-114">-DefaultProfile</span></span>
<span data-ttu-id="e4b0f-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e4b0f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4b0f-116">-FilePath</span><span class="sxs-lookup"><span data-stu-id="e4b0f-116">-FilePath</span></span>
<span data-ttu-id="e4b0f-117">Путь к JSON-файлу, содержащего SQL определения политики защиты информации.</span><span class="sxs-lookup"><span data-stu-id="e4b0f-117">Specifies a path of a .json file containing SQL Information Protection Policy definition.</span></span>

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

### <span data-ttu-id="e4b0f-118">-Политика</span><span class="sxs-lookup"><span data-stu-id="e4b0f-118">-Policy</span></span>
<span data-ttu-id="e4b0f-119">Определяет определение политики SQL защиты информации.</span><span class="sxs-lookup"><span data-stu-id="e4b0f-119">Specifies a SQL information protection policy definition.</span></span> <span data-ttu-id="e4b0f-120">Вы можете указать путь к JSON-файлу или строке, определяемой политикой в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="e4b0f-120">You can specify a path of a .json file or a JSON format string that defines the policy.</span></span>

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

### <span data-ttu-id="e4b0f-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e4b0f-121">-Confirm</span></span>
<span data-ttu-id="e4b0f-122">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4b0f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4b0f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4b0f-123">-WhatIf</span></span>
<span data-ttu-id="e4b0f-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4b0f-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e4b0f-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="e4b0f-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4b0f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4b0f-126">CommonParameters</span></span>
<span data-ttu-id="e4b0f-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4b0f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4b0f-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e4b0f-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4b0f-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e4b0f-129">INPUTS</span></span>

### <span data-ttu-id="e4b0f-130">System.String</span><span class="sxs-lookup"><span data-stu-id="e4b0f-130">System.String</span></span>

## <span data-ttu-id="e4b0f-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e4b0f-131">OUTPUTS</span></span>

### <span data-ttu-id="e4b0f-132">Microsoft.Azure.Commands.SecurityCenter.Models.SqlInformationProtectionPolicy.PSSqlInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="e4b0f-132">Microsoft.Azure.Commands.SecurityCenter.Models.SqlInformationProtectionPolicy.PSSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="e4b0f-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e4b0f-133">NOTES</span></span>

## <span data-ttu-id="e4b0f-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e4b0f-134">RELATED LINKS</span></span>