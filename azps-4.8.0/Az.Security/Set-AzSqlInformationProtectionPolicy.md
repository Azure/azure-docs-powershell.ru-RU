---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSqlInformationProtectionPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSqlInformationProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSqlInformationProtectionPolicy.md
ms.openlocfilehash: 3b433860cda56f827bb58bc135240da41b89ef93
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235340"
---
# <span data-ttu-id="b22f9-101">Set-AzSqlInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="b22f9-101">Set-AzSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="b22f9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b22f9-102">SYNOPSIS</span></span>
<span data-ttu-id="b22f9-103">Установка действующей политики защиты данных SQL для клиента.</span><span class="sxs-lookup"><span data-stu-id="b22f9-103">Sets the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="b22f9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b22f9-104">SYNTAX</span></span>

### <span data-ttu-id="b22f9-105">Политика защиты данных SQL (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b22f9-105">SQL Information Protection Policy (Default)</span></span>
```
Set-AzSqlInformationProtectionPolicy -Policy <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b22f9-106">Путь к файлу политики защиты данных SQL</span><span class="sxs-lookup"><span data-stu-id="b22f9-106">SQL Information Protection Policy File Path</span></span>
```
Set-AzSqlInformationProtectionPolicy -FilePath <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b22f9-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b22f9-107">DESCRIPTION</span></span>
<span data-ttu-id="b22f9-108">Установка действующей политики защиты данных SQL для клиента.</span><span class="sxs-lookup"><span data-stu-id="b22f9-108">Sets the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="b22f9-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b22f9-109">EXAMPLES</span></span>

### <span data-ttu-id="b22f9-110">Образом</span><span class="sxs-lookup"><span data-stu-id="b22f9-110">Example</span></span>
```powershell
PS C:\> Set-AzSqlInformationProtectionPolicy -FilePath "C:\Users\myUser\Desktop\policy.json"
```

## <span data-ttu-id="b22f9-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b22f9-111">PARAMETERS</span></span>

### <span data-ttu-id="b22f9-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b22f9-112">-AsJob</span></span>
<span data-ttu-id="b22f9-113">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="b22f9-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b22f9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b22f9-114">-DefaultProfile</span></span>
<span data-ttu-id="b22f9-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b22f9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b22f9-116">-FilePath</span><span class="sxs-lookup"><span data-stu-id="b22f9-116">-FilePath</span></span>
<span data-ttu-id="b22f9-117">Задает путь к файлу JSON, содержащему определение политики защиты информации SQL.</span><span class="sxs-lookup"><span data-stu-id="b22f9-117">Specifies a path of a .json file containing SQL Information Protection Policy definition.</span></span>

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

### <span data-ttu-id="b22f9-118">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="b22f9-118">-Policy</span></span>
<span data-ttu-id="b22f9-119">Задает определение политики защиты данных SQL.</span><span class="sxs-lookup"><span data-stu-id="b22f9-119">Specifies a SQL information protection policy definition.</span></span> <span data-ttu-id="b22f9-120">Вы можете указать путь к JSON-файлу или строку формата JSON, определяющую политику.</span><span class="sxs-lookup"><span data-stu-id="b22f9-120">You can specify a path of a .json file or a JSON format string that defines the policy.</span></span>

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

### <span data-ttu-id="b22f9-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b22f9-121">-Confirm</span></span>
<span data-ttu-id="b22f9-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b22f9-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b22f9-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b22f9-123">-WhatIf</span></span>
<span data-ttu-id="b22f9-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b22f9-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b22f9-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b22f9-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b22f9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b22f9-126">CommonParameters</span></span>
<span data-ttu-id="b22f9-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b22f9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b22f9-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b22f9-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b22f9-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b22f9-129">INPUTS</span></span>

### <span data-ttu-id="b22f9-130">System. String</span><span class="sxs-lookup"><span data-stu-id="b22f9-130">System.String</span></span>

## <span data-ttu-id="b22f9-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b22f9-131">OUTPUTS</span></span>

### <span data-ttu-id="b22f9-132">Microsoft. Azure. Commands. SecurityCenter. Models. SqlInformationProtectionPolicy. PSSqlInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="b22f9-132">Microsoft.Azure.Commands.SecurityCenter.Models.SqlInformationProtectionPolicy.PSSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="b22f9-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="b22f9-133">NOTES</span></span>

## <span data-ttu-id="b22f9-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b22f9-134">RELATED LINKS</span></span>
