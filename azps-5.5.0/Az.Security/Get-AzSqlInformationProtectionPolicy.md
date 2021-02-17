---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSqlInformationProtectionPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSqlInformationProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSqlInformationProtectionPolicy.md
ms.openlocfilehash: 7f84c3b10577eea0d035c2ce84b3aa8a61af4a3d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100232793"
---
# <span data-ttu-id="9d572-101">Get-AzSqlInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="9d572-101">Get-AzSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="9d572-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d572-102">SYNOPSIS</span></span>
<span data-ttu-id="9d572-103">Извлекает эффективную политику защиты информации SQL клиента.</span><span class="sxs-lookup"><span data-stu-id="9d572-103">Retrieves the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="9d572-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9d572-104">SYNTAX</span></span>

```
Get-AzSqlInformationProtectionPolicy [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9d572-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9d572-105">DESCRIPTION</span></span>
<span data-ttu-id="9d572-106">Извлекает эффективную политику защиты информации SQL клиента.</span><span class="sxs-lookup"><span data-stu-id="9d572-106">Retrieves the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="9d572-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9d572-107">EXAMPLES</span></span>

### <span data-ttu-id="9d572-108">Пример</span><span class="sxs-lookup"><span data-stu-id="9d572-108">Example</span></span>
```powershell
PS C:\> Get-AzSqlInformationProtectionPolicy
```

## <span data-ttu-id="9d572-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9d572-109">PARAMETERS</span></span>

### <span data-ttu-id="9d572-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9d572-110">-AsJob</span></span>
<span data-ttu-id="9d572-111">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="9d572-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9d572-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d572-112">-DefaultProfile</span></span>
<span data-ttu-id="9d572-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9d572-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9d572-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d572-114">CommonParameters</span></span>
<span data-ttu-id="9d572-115">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d572-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d572-116">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9d572-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d572-117">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9d572-117">INPUTS</span></span>

### <span data-ttu-id="9d572-118">System.string</span><span class="sxs-lookup"><span data-stu-id="9d572-118">System.string</span></span>

## <span data-ttu-id="9d572-119">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9d572-119">OUTPUTS</span></span>

### <span data-ttu-id="9d572-120">Microsoft.Azure.Commands.SecurityCenter.Models.SqlInformationProtectionPolicy.PSSqlInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="9d572-120">Microsoft.Azure.Commands.SecurityCenter.Models.SqlInformationProtectionPolicy.PSSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="9d572-121">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9d572-121">NOTES</span></span>

## <span data-ttu-id="9d572-122">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9d572-122">RELATED LINKS</span></span>
