---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B30C2BDD-6DA9-47B5-88FE-3AD43E15A072
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmsqlserverkeyvaultcredentialconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerKeyVaultCredentialConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerKeyVaultCredentialConfig.md
ms.openlocfilehash: 50bf29524e4c16a7a7186a547505f4dcf7dac4e2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245723"
---
# <span data-ttu-id="16397-101">New-AzVMSqlServerKeyVaultCredentialConfig</span><span class="sxs-lookup"><span data-stu-id="16397-101">New-AzVMSqlServerKeyVaultCredentialConfig</span></span>

## <span data-ttu-id="16397-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="16397-102">SYNOPSIS</span></span>
<span data-ttu-id="16397-103">Создает объект конфигурации для учетных данных хранилища ключей SQL Server на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="16397-103">Creates a configuration object for SQL server key vault credential on a virtual machine.</span></span>

## <span data-ttu-id="16397-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="16397-104">SYNTAX</span></span>

```
New-AzVMSqlServerKeyVaultCredentialConfig [-ResourceGroupName] <String> [-Enable] [-CredentialName <String>]
 [-AzureKeyVaultUrl <String>] [-ServicePrincipalName <String>] [-ServicePrincipalSecret <SecureString>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16397-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="16397-105">DESCRIPTION</span></span>

## <span data-ttu-id="16397-106">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="16397-106">EXAMPLES</span></span>

## <span data-ttu-id="16397-107">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="16397-107">PARAMETERS</span></span>

### <span data-ttu-id="16397-108">-AzureKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="16397-108">-AzureKeyVaultUrl</span></span>
<span data-ttu-id="16397-109">URL-адрес службы хранилища ключей Azure</span><span class="sxs-lookup"><span data-stu-id="16397-109">Azure Key Vault service URL</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16397-110">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="16397-110">-CredentialName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16397-111">-Enable (включить)</span><span class="sxs-lookup"><span data-stu-id="16397-111">-Enable</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16397-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16397-112">-ResourceGroupName</span></span>
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

### <span data-ttu-id="16397-113">-Намерено</span><span class="sxs-lookup"><span data-stu-id="16397-113">-ServicePrincipalName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16397-114">-ServicePrincipalSecret</span><span class="sxs-lookup"><span data-stu-id="16397-114">-ServicePrincipalSecret</span></span>
```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16397-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="16397-115">-Confirm</span></span>
<span data-ttu-id="16397-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="16397-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16397-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16397-117">-WhatIf</span></span>
<span data-ttu-id="16397-118">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="16397-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16397-119">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="16397-119">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16397-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16397-120">CommonParameters</span></span>
<span data-ttu-id="16397-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="16397-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16397-122">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="16397-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16397-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="16397-123">INPUTS</span></span>

### <span data-ttu-id="16397-124">System. String</span><span class="sxs-lookup"><span data-stu-id="16397-124">System.String</span></span>

### <span data-ttu-id="16397-125">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="16397-125">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="16397-126">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="16397-126">System.Security.SecureString</span></span>

## <span data-ttu-id="16397-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="16397-127">OUTPUTS</span></span>

### <span data-ttu-id="16397-128">Microsoft. Azure. Commands. COMPUTE. KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="16397-128">Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings</span></span>

## <span data-ttu-id="16397-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="16397-129">NOTES</span></span>

## <span data-ttu-id="16397-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="16397-130">RELATED LINKS</span></span>
